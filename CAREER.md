# Kim NOËL — Professional Profile

> Structured career summary designed to be easily parsed by humans and AI assistants.
> Sources: CVs (Sep. and Oct. 2026) and LinkedIn profile.
> Client names of Artik Consulting are anonymized and replaced by their industry.

## Identity

| Field | Value |
|---|---|
| Name | Kim NOËL (initials: KNO) |
| Current title | AI & LLM Engineer / AI Architect |
| Employer | Artik Consulting (IT consulting firm, Paris) — permanent contract since Mar 2019 |
| Location | Paris, France (hybrid) |
| Total experience | 12 years (since 2014) |
| LinkedIn | https://www.linkedin.com/in/kimnoel |
| GitHub | https://github.com/knoel99 |
| Languages | French (native), English (fluent — TOEFL iBT 93/120, TOEIC 960/990), Spanish (professional, can lead meetings), Arabic (self-taught) |

## Summary

AI & LLM engineer with 12 years of experience, combining a scientific engineering background (geosciences, geomechanics, numerical simulation) with 7+ years of consulting in Big Data and generative AI.
Builds production-grade LLM applications (RAG, agents, MCP servers, classification), runs the infrastructure underneath them (on-prem GPUs, Kubernetes, Azure) and keeps them under control (FinOps, observability, security, EU AI Act compliance).
Early LLM advocate (since March 2023), technical speaker, writer and university lecturer on generative AI.

## Core competencies

- **Applied generative AI**: RAG chatbots, autonomous agents (smolagents, LangChain, ReAct), MCP servers, agent skills, headless coding agents, LLM-based text classification, OCR + LLM extraction, prompt engineering, speech-to-speech.
- **LLM infrastructure / AIOps**: on-prem GPU inference (NVIDIA), vLLM, llama.cpp, LiteLLM gateway, Kubernetes/Helm, CI/CD, GPU benchmarking (DCGM, gpu-burn), LLM deployment on AWS, Azure, GCP and Hugging Face Endpoints.
- **GenAI FinOps & observability**: token and GPU cost tracking, budgets, SLI/SLO, Prometheus, Grafana, Loki.
- **Cloud**: Azure (Azure OpenAI, AI Search, Function Apps, private networking), Terraform.
- **AI governance & security**: EU AI Act compliance tooling, CVE automation, data anonymization, Kerberos, Zero Trust.
- **Data engineering**: Kafka Streams, Spring Boot microservices, Cassandra, Elasticsearch, Cloudera (HDFS, Spark, Hive), OpenShift.
- **Consulting**: requirements gathering, technical scoping, solution architecture, workshops with business teams, public speaking.

## Career timeline

| Period | Company | Role | Client sector |
|---|---|---|---|
| Aug 2025 – present | Artik Consulting | AI Engineer on Azure | Public legal institution |
| Aug 2024 – present | Artik Consulting | Lead AI Engineer (LLM) | Public social-economic institution |
| 2023 – present | EPF Engineering School | Lecturer, M2 AI / LLM | Higher education |
| Mar 2023 – present | Artik Consulting | LLM Advocate & technical speaker | Internal + major logistics enterprise |
| Mar 2023 – Jul 2023 | Artik Consulting | AI Engineer (remote) | International economic organization |
| Apr 2022 – 2024 | Artik Consulting | Lead Data Engineer | Major logistics enterprise |
| Mar 2019 – Mar 2022 | Artik Consulting | Data Engineer / Data Scientist / Solution Architect | Major logistics enterprise + other clients |
| Sep 2014 – Aug 2018 | Curistec (Lyon area) | Product Owner of a simulation software & R&D Engineer | Oil & gas |
| Mar 2014 – Aug 2014 | Curistec | R&D Engineer Intern (master thesis) | Oil & gas |
| Jun 2013 – Aug 2013 | Curistec | Product Owner Intern | — |
| 2012 | SCREG | Student job | — |

---

## Detailed experience

### Artik Consulting — Big Data & AI/LLM Consultant (Mar 2019 – present)

#### 1. Lead AI Engineer — Public social-economic institution (Aug 2024 – present)

- **Context**: French public body in the social protection sector. Artik was hired to gather business requirements, then scope and build generative AI solutions.
- **Projects**:
  - **DevOps**: modernized and automated the deployment infrastructure with CI/CD pipelines on Kubernetes (Helm, Docker), reducing deployment time from 1 h to 5 min; SLI/SLO and usage dashboards (Prometheus, Grafana, Loki); production alerting and incident management.
  - **Website content summaries**: app that automatically generates SEO summaries whenever the organization's website publishes new content (e.g. press releases); requirements gathered with journalists, prompts tuned per topic with business teams, integrated with the existing CMS, deployed to production with token FinOps tracking. Saves the editorial team hours of writing.
  - **Security automation (CISO / CVE)**: automated CVE collection for the application stack with auto-generated Jira tickets; headless agent processes tickets via MCP and opens pull requests for human approval; shared agent skill pre-fills the CISO's security form for validation; rapid response to the LiteLLM supply-chain compromise (April 2026).
  - **MCP server for Cloudera**: natural-language querying of enterprise data; MCP server connected to Cloudera CML via Kerberos so agents inherit exactly the user's access rights; usable from GitHub Copilot; designed, built and deployed in one day during an internal hackathon.
  - **EU AI Act compliance tool**: governance app where an LLM reads a project's documentation or code, fills in the European Commission's official form, assesses the risk level (out of scope / high risk / prohibited) and justifies each answer; human-reviewed outputs; Jira integration creates action tickets for each regulatory obligation.
  - **Advanced text classification**: LLM classification of 700,000 records for an economic study on natural disasters, where traditional ML failed — accuracy raised from 55% to 96%; benchmark of zero-shot classifiers vs. open-weight and proprietary LLMs; data anonymized before processing; results loaded into HDFS. The study was published by the institution in April 2025, with KNO as co-author.
  - **Country profiles (research agents)**: autonomous agents (smolagents, Hugging Face) that research and write reports on social insurance systems worldwide with validated citation tracking; turnaround cut from several weeks to a few hours of proofreading; coverage extended to 150 countries.
  - **AI Week (robotics)**: Reachy Mini robot hosting employee AI-awareness events; benchmark of speech-to-text vs. speech-to-speech on performance, cost and latency (OpenAI gpt-realtime selected); robot reacts with movements and emotions matching visitors' speech.
  - **Audience data**: Python app that scrapes usage data of the organization's published datasets and generates dynamic Excel charts and PowerPoint slides; containerized and deployed on managed Kubernetes.
  - **Developer productivity**: specified, built and shared agents, skills and MCP servers automating repetitive tasks for developers and managers.
- **Stack**: Python 3.10+, Bash · Kubernetes, Rancher, Helm, Docker · LiteLLM, vLLM, llama.cpp, OpenAI API, Hugging Face, smolagents, LangChain, Llama 3.1, Mixtral, MCP · Prometheus, Grafana, Loki · Cloudera on-prem (HDFS, Spark/PySpark, Hive, Hue, CML), OpenDataSoft · FastAPI, Gradio, Dash, Tavily · Jira, Kerberos, Zero Trust.

#### 2. AI Engineer on Azure — Public legal institution (Aug 2025 – present)

- **Context**: French public legal institution deploying a chatbot that queries both public regulatory texts and a highly confidential private document base.
- **Achievements**:
  - Designed a scalable, cost-aware RAG chatbot architecture on Azure (indexing, retrieval, reranking, orchestration) with explicit trade-offs on cost, latency and security.
  - Secured the solution: confidential documents in an Azure private network, unreachable from outside even with an API key; private Azure OpenAI endpoint.
  - GenAI FinOps: Azure OpenAI token spend monitoring and budget alerts; right-sized AI Search and Function Apps consumption; RAG cost optimization (context limits, caching of frequent queries, no redundant re-indexing); cost dashboards and spend reviews for business and IT.
  - Automated updates of regulatory texts via Function Apps calling the Légifrance and Judilibre public APIs.
  - Infrastructure as code with Terraform; administration of the Open WebUI front end and OAuth access rights.
  - Led scoping workshops with the client and business teams.
- **Stack**: Python, Azure, Azure OpenAI, Azure AI Search, Azure Function Apps, Azure cost monitoring, Open WebUI, Terraform, web scraping.

#### 3. LLM Advocate & Technical Speaker (Mar 2023 – present)

- **Context**: from early 2023, Artik Consulting anticipated that LLMs would become critical for its clients' technology roadmap; KNO took the role of internal and external LLM advocate.
- **Achievements**:
  - **GPT vs. human developers (Mar 2023)**: entered GPT-3.5 and GPT-4 in the "Le Meilleur Dev de France" coding contest; GPT-3.5 failed to qualify, GPT-4 reached the final and ranked 44th / 175 finalists; results published as an article on the Artik blog.
  - **Big Data & AI Paris trade show (Sep 2023)**: 30-minute public talk comparing proprietary and open-source LLMs; lessons learned from deploying open-weight LLMs on AWS, Azure, GCP and Hugging Face Endpoints; importance of GPUs and rental costs; viable ChatGPT alternatives for companies (e.g. llama.cpp).
  - **10+ keynotes** on AI, LLMs, GPUs and AI governance to 1,000+ professionals at industry conferences and enterprise workshops.
  - Daily technology watch (r/LocalLLaMA, key researchers and builders); wrote a white paper on LLMs.
  - **For a major logistics enterprise client (2023 – 2024)**: assessed AI use cases before project launch (early detection of logistics incidents via NLP on emails, smoother parcel-claims handling, image generation for marketing); animated the AI community (webinars for IT departments, generative/agentic AI overviews for the architects' community of practice, GitHub Copilot demos for developers and product owners); represented the IT department at an internal innovation forum (June 2024), with subsidiaries on their AI projects, and with the group legal team on the EU AI Act.

#### 4. AI Engineer — International economic organization (Mar 2023 – Jul 2023, remote)

- **Context**: to make its economic and social data more accessible, the organization built a chatbot proof of concept interfacing with its databases for statisticians.
- **Achievements**: review of the 2023 LLM landscape; chatbot selected and deployed as a ChatGPT Plugin; RAG tests on vector databases with text and statistical (SDMX) data.
- **Stack**: Python 3.10, FastAPI, Poetry, ChatGPT Plugins, RAG, Weaviate, Pinecone, SDMX.

#### 5. Data Engineer then Lead Data Engineer — Major logistics enterprise (Mar 2019 – 2024)

- **Context**: full overhaul of the IT system with a Big Data, event-driven architecture. Data Engineer from Mar 2019 to Mar 2022, Lead Data Engineer from Apr 2022.
- **Achievements**:
  - Architected and optimized a distributed system of 100–120+ microservices processing 10M+ events per day, released weekly on OpenShift (Kubernetes).
  - Led an infrastructure transformation that cut critical incidents by 94% (from every two weeks to once per quarter) through systematic refactoring and proactive monitoring.
  - DevOps / SRE: production stability, incident resolution, data recovery after outages; KPI/SLI dashboards (Prometheus, Kibana, Grafana) used by business teams; JVM tuning, Kafka Streams thread/consumer sizing aligned with partitions; CI/CD (Jenkins, GitLab CI, Docker).
  - Lead data engineer: helped product owners write technical specifications in SAFe ceremonies; documented business rules and redesigned data flows; built a Spring Boot indexing microservice to trace data flows; close collaboration with product owners.
- **Stack**: Java, Spring Boot, Kafka Streams, Cassandra, Elasticsearch, OpenShift/Kubernetes, Docker, Jenkins, GitLab CI, Git, Prometheus, Kibana, Grafana, SAFe, Jira, Confluence.

#### 6. Data Scientist and Solution Architect — Various clients (2019 – 2022)

- **Data Scientist**: built a proof of concept of an OCR and text-analysis tool extracting key data from receipts; deployed it in production inside the company's existing web platform, cutting monthly expense-report processing from 1 hour to 5 minutes. Stack: Python, PHP, JavaScript.
- **Solution Architect**: reworked the architecture of clients in core banking, customer mediation and logistics; delivered a blueprint with a selection of the best technologies and development kit for each context.

### EPF Engineering School — Lecturer, M2 AI / LLM (2023 – present)

Two-day course for M2 students of the Digital Engineering major (cybersecurity and AI track): introduction to neural networks and the state of generative AI; inference hardware and software; lessons learned from enterprise GenAI projects.

### Curistec — Geomechanics and Numerical Simulation (Jun 2013 – Aug 2018)

Company near Lyon (Saint-Didier-au-Mont-d'Or) developing well-integrity simulation software for oil & gas clients (incl. BP and Total).

- **Product Owner of a simulation software (Sep 2014 – Aug 2018, permanent contract)**:
  - Designed and managed simulation software for oil-well mechanical integrity, used to optimize material sizing.
  - Led a cross-functional international team of 5 engineers: technical roadmap and specifications.
  - Coordinated teams and clients in Spain and the UK; ran workshops and meetings in English and Spanish.
  - Ticket triage, prioritization, maintenance, documentation and customer support.
  - Developed original mathematical and physical models; a resulting scientific paper (SPE) ranked in the top 10 most downloaded in its field and was presented at international conferences.
  - Stack: Java, V-model.
- **R&D Engineer Intern (Mar 2014 – Aug 2014)**: master thesis "Formation and propagation of a micro-annulus in a cement sheath due to fluid injection" — hydraulic fracturing modeling, gas migration. International mobility: Hanoi, Vietnam (2 months).
- **Product Owner Intern (Jun 2013 – Aug 2013)**: specifications and upgrade of a Laboratory Information Management System (LIMS).

### Student job (2012)

- Construction worker — SCREG, Villepinte (Jul – Aug 2012).

---

## Education

| Period | School | Degree | Notes |
|---|---|---|---|
| 2018 – 2019 | IFP School & ENSG Géomatique, Paris | Specialized degree in Petroleum Data Management | GPA 3.73/4; courses: georesources, E&P data, data management, geomatics, GIS, IT; sponsored by Total |
| 2011 – 2014 | Polytech Sorbonne (Paris 6) | Engineer's degree, Geological and Earth Sciences / Geosciences | GPA 3.0/4.0; Junior Entreprise (Vice Treasurer); Total Student Ambassador (1 year); Total Summer School; 6-month project with IFP School on reservoir rock volume evaluation from seismic records |
| — | CNAM (evening classes) | Continuing education in computer science | UTC503 Programming paradigms, UTC504 Information systems and databases, UTC505 Networks and security |

## Certifications

27 certifications (source: LinkedIn). Credential IDs are given when available.

### AI, cloud and FinOps

| Date | Certification | Issuer | Credential ID |
|---|---|---|---|
| Oct 2026 (expires Oct 2028) | FinOps Certified: FinOps for AI (certificate title: "AI Value") | FinOps Foundation | dworuserr5rr |
| Sep 2026 | Microsoft Certified: Azure AI Fundamentals (AI-901) | Microsoft | 23F0E1F7CA8E504E |
| Sep 2026 | Microsoft Certified: Azure Fundamentals (AZ-900) | Microsoft | CAC8C511BCC6ECDF |
| Jul 2025 | Claude with the Anthropic API | Anthropic | avsqbr8yj2yr |
| Feb 2025 | AI Agents Fundamentals | Hugging Face | knoel |

### Data, IT and software engineering

| Date | Certification | Issuer | Credential ID |
|---|---|---|---|
| Jul 2019 | Google IT Support Professional Certificate | Coursera (Google) | — |
| Jul 2019 | IT Security: Defense against the digital dark arts | Coursera (Google) | ZVD43UH8XGCT |
| Jul 2019 | System Administration and IT Infrastructure Services | Coursera (Google) | 7EEFTXSV9X2X |
| Jul 2019 | Operating Systems and You: Becoming a Power User | Coursera (Google) | R49MXZC5DJJQ |
| Jun 2019 | The Bits and Bytes of Computer Networking | Coursera (Google) | BVSH755G4C54 |
| May 2019 | Technical Support Fundamentals | Coursera (Google) | 7QGMNBT4DK2G |
| Mar 2019 (expired Mar 2024) | Data Management Fundamentals | DAMA International | — |
| Feb 2019 | Introduction to Master Data Management | PPDM Association | 12542038 |
| Jan 2019 | Hadoop Starter Kit | Udemy | UC-AFD3J9TL |
| Dec 2018 | Introduction to Python for Data Science | edX | d6fee0afeb74456abdcf66285611bd82 |
| Dec 2018 | Python 3: fundamentals to advanced concepts | Université Côte d'Azur | — |
| Oct 2018 | Introduction to statistics with R | Université Paris-Sud | — |
| Jul 2018 | Data Science and Data Engineering Bootcamp | Data Science Dojo | — |
| Jul 2017 | An introduction to SDMX for data producers | Stat Academy | — |
| Jun 2016 | Quality in Enterprise Software Development | INSAVALOR | FAFIEC 22682 |
| May 2016 | Java development | DMR | — |

### Energy and geosciences

| Date | Certification | Issuer | Credential ID |
|---|---|---|---|
| Dec 2017 | MOOC Oil & Gas 3 — Certificate of achievement | IFP School | — |
| Jun 2017 | Statement of Accomplishment in Reservoir Geomechanics | Stanford University | 246224772d7546e88af07ce45133bc6b |

### Languages and other

| Date | Certification | Issuer | Credential ID |
|---|---|---|---|
| Jul 2019 | Mode et style (MOOC) | Conservatoire National des Arts et Métiers (CNAM) | — |
| Mar 2019 | War strategy | École Pratique des Hautes Études (EPHE) | — |
| May 2013 (expired May 2014) | TOEIC 945/990 | ETS EMEA | — |
| Oct 2012 (expired Oct 2014) | TOEFL iBT 93/120 | ETS EMEA | 0000 0000 1680 9977 |

## Awards and hackathons

| Date | Event | Result | Details |
|---|---|---|---|
| Apr 2024 | Mistral AI hackathon | 4th / 12 teams | Turned municipal decrees about road events into DATEX II structured data: OCR on unstructured documents (Pytesseract), Mistral-large formatting, ReAct framework for output quality |
| Mar 2023 | Le Meilleur Dev de France | 70th / 153 (qualification round) | Coding contest |
| May 2019 | Data Science Olympics | 217th / 1,000 | Emmaüs dataset |
| Mar 2019 | School of AI health hackathon | 2nd / 8 best presentation, 4th / 8 best team | Protein folding problem |
| Jul 2018 | Data Science Dojo | 5th / 40 | Titanic dataset |
| 2018 – 2019 | Total | Sponsorship | IFP School sponsorship, Total Student Ambassador, Total Summer School |
| — | Internal hackathon (public social-economic institution) | Delivered | MCP server for Cloudera designed, built and deployed in one day |

## Publications

| Date | Title | Venue |
|---|---|---|
| Apr 2025 | Economic study on natural disasters and the use of short-time work schemes (co-author) | Client institution (public social-economic) |
| Apr 2023 | "J'ai fait coder ChatGPT-4 contre le meilleur Dev de France (et c'est un carnage)" | Artik Consulting blog |
| Jul 2022 | "Du Plan Calcul de De Gaulle à la Startup Nation de Macron : une rétrospective de l'informatique en France (2/2)" | Artik Consulting blog |
| Jan 2021 | "4 things to do to fail your career transition into Big Data" | Medium |
| Nov 2020 | "Du Plan Calcul de De Gaulle à la Startup Nation de Macron : une rétrospective de l'informatique en France (1/2)" | Artik Consulting blog |
| Mar 2020 | "10 femmes qui vont révolutionner l'informatique en 2020" | Artik Consulting blog |
| Apr 2019 | "Comment un débutant en IA a pu finir 4ème dans un hackathon mondial (School of AI)" | Medium |
| Mar 2019 | "YouTube pour comprendre le Deep Learning et les réseaux de neurones" | Medium |
| 2018 | SPE-191335-MS: "Cement Plug Hydraulic Integrity — The Ultimate Objective of Cement Plug Integrity" (co-author) | Society of Petroleum Engineers |
| Oct 2015 | "Taking holistic approach to designing cement sheaths helps maintain zonal isolation for life of well, increases ROI" (Curistec authors) | Drilling Contractor |

## Recommendation

- **Oct 2018 — Well cementing advisor, client of Curistec**: "I have worked with Kim on a software development project. Kim demonstrated exceptional project management abilities and exceeded expectations with regards to service delivery. The project was concluded successfully and in time."

## Volunteering

- Volunteer — French Red Cross (Croix-Rouge française), Dec 2008 – Mar 2009: missions and events for disadvantaged children.

## Skills (flat list)

- **Languages**: Python, Java, Bash, SQL, R, PHP, JavaScript, HTML, Fortran
- **AI / LLM**: Claude / Anthropic API, OpenAI API / ChatGPT, Azure OpenAI, Mistral, Hugging Face, smolagents, LangChain, ReAct, agents, MCP, vLLM, llama.cpp, LiteLLM, Llama 3.1, Mixtral, RAG, OCR (Pytesseract), zero-shot classification, prompt engineering, agent harnesses, Claude Code, GitHub Copilot, machine learning, data science
- **Local AI**: GPU inference, NVIDIA and AMD hardware (self-taught)
- **Infrastructure**: Kubernetes, Helm, Rancher, OpenShift, Docker, Terraform, Azure, AWS, GCP, Jenkins, GitLab CI
- **Data**: Big Data, data engineering, microservices, Kafka / Kafka Streams, Cassandra, Elasticsearch, MySQL, Cloudera (HDFS, Spark, Hive, CML), Hadoop, OpenDataSoft, SDMX, DATEX II, master data management
- **Observability / FinOps**: FinOps for AI, Prometheus, Grafana, Loki, Kibana, DCGM, LiteLLM budgets
- **Apps & APIs**: FastAPI, Spring Boot, Gradio, Dash, Open WebUI, REST APIs
- **Geosciences & energy**: petroleum engineering, geomechanics, rock mechanics, geophysics, earth science, GIS, oil & gas
- **Office**: Microsoft Excel, PowerPoint
- **Methods**: Agile, Scrum, Kanban, SAFe, V-model, Jira, Confluence, Git
- **Soft skills**: teamwork, curiosity, management, research, analysis, commitment

### Most endorsed skills on LinkedIn (43 skills listed)

| Skill | Endorsements |
|---|---|
| Teamwork | 8 (incl. 2 Artik Consulting colleagues) |
| Curiosity | 8 |
| Microsoft Excel | 5 (incl. 3 Curistec colleagues) |
| Petroleum | 4 (incl. 3 Curistec colleagues) |
| Rock Mechanics | 4 (incl. 2 Curistec colleagues) |
| Energy | 4 |
| Geophysics | 3 |
| Engineering | 3 |
| Geomechanics | 2 (incl. 2 Curistec colleagues) |
| Management | 2 (incl. 2 Curistec colleagues) |
| English, Research, Analysis | 2 each |
| Big Data, Java, Spring Boot, Apache Kafka, Kafka Streams, PowerPoint | 1 each |

## Interests

- Tech news (X, Reddit r/LocalLLaMA)
- Robotics: Reachy Mini, Microduck
- Audiobooks, especially biographies
