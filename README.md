# CHATDB-THE FUTURE OF BUSINESS INTELLIGENCE

## Introduction

Large language models (LLMs) exhibit an impressive capability to comprehend prompts in natural language and produce coherent responses. This ability has introduced fresh opportunities for transforming natural language into structured query languages, such as SQL. Unlike previously, where crafting SQL queries necessitated technical proficiency, LLMs empower users to articulate their inputs in simple English, enabling the automatic generation of the corresponding SQL code.

ChatDB is a framework that empowers users to talk to their data, no matter their technical background. It leverages the power of large language models (LLMs) to understand natural language questions and translate them into complex database queries, automatically.

It enables users to chat with their in-house data assets in a conversational manner, simplifying data access and analysis within an organization. The interactive interface of ChatDB provides a user-friendly platform for non-technical users to interact with their in-house data assets using natural language, making data querying more accessible and intuitive.

## Key Features

Key features of ChatDB:

1. **Conversational Interface:** ChatDB offers a user-friendly and intuitive conversational interface, allowing non-technical users to interact with complex databases using natural language effortlessly.
2. **Easy Onboarding:** The platform provides interactive tools that simplify the onboarding process, enabling users to get started with the system quickly and efficiently.
3. **Connection With Various Data Warehouses:** ChatDB seamlessly connects to various data warehouses, both cloud-based and on-premise, unlocking the power of your entire data ecosystem.
4. **Integration of Symbolic Memory with LLMs:** ChatDB seamlessly integrates symbolic memory with Language Model (LLM) technology, enhancing its capability to handle large data sets and schemas with ease.
5. **Chain-of-Memory Framework:** The framework comprises three main stages - input processing, chain-of-memory, and response summary. This structure enables ChatDB to manipulate external memory, execute SQL statements, and deliver final responses based on the results of the memory chain seamlessly.

## Use Case Examples

To demonstrate the capabilities of ChatDB, we utilized real-world datasets from the DHIS2 system, which serves as the Kenyan health management information system, encompassing a diverse range of healthcare data nationwide.

Our demonstration harnessed 5 years of historical data, focusing on key Performance Indicators (KPIs) such as Fresh Still Birth Rate and Facility Maternal Mortality Ratio. These datasets span various counties and sub-counties in Kenya, offering a comprehensive overview of healthcare trends.

**What Was Achieved:**

1. **Intuitive Exploration:** Users, regardless of their technical expertise, could effortlessly inquire about the data using natural language. For example, they could ask questions like, "What is the trend of Fresh Still Birth Rate in rural counties over the past 3 years?"
2. **Meaningful Insights:** ChatDB processed intricate queries, extracting insights and identifying correlations within the data. Users received not only raw data but also understandable responses.
3. **County-Level Analysis:** Users had the ability to delve into specific counties and sub-counties, comparing performance and pinpointing areas requiring attention.
4. **Time-Series Analysis:** ChatDB conducted thorough analyses of trends and patterns over time, enabling users to comprehend how KPIs have evolved over the past 5 years.

## Technical Implementation

The LLM agent is built using Llama Index which is a data framework designed to facilitate the integration of custom data sources with large language models (LLMs). When the Data LLM agent receives a query, it performs a sequence of steps:

- First, the Data LLM Agent queries the Object Index retriever and gets the relevant tables and their metadata needed to answer the question.
- Second, the agent takes the help of an LLM – be it OpenAI, Claude, Palm, Llama2, NSQL, etc – to form the SQL query for your data warehouse to answer the question.
- Third, the agent queries your data warehouse using the connector and fetches the relevant data.
- Finally, the agents use an LLM to summarize the results to answer the question asked by the user and responds back.

An illustration for the setup and working of the Data LLM AI Agent is shown below:

![Illustration](RackMultipart20240211-1-dgvvei_html_27e6ef8ebcf43f23.png)

## Benefits For Users

**For Individuals:**

- **Democratized Data Access:** Access and analyze data regardless of technical background, eliminating the need to learn complex querying languages.
- **Greater Self-Sufficiency:** Find answers and insights without relying on technical specialists, enhancing independence in data exploration.
- **Improved Decision-Making:** Quick access to data facilitates faster and informed decision-making processes.
- **Increased Confidence in Analysis:** Understanding how queries translate into SQL builds trust in the obtained results.

**For Organizations:**

- **Increased Data Utilization:** More personnel can access and utilize data, optimizing valuable assets.
- **Improved Productivity:** Less time spent on learning SQL allows more focus on data analysis and insights derivation.
- **Reduced Costs:** Decreased need for specialized data professionals or expensive analysis tools.
- **Enhanced Collaboration:** Natural language querying fosters communication and collaboration between technical and non-technical teams.
- **More Informed Decision-Making:** Data-driven insights readily available to inform strategic decisions at all levels within the organization.

## Future RoadMap

1. **Visual Graph and Chart Generation:**

   **Benefits:**
   - Enhanced understanding: Visualizations can effectively represent complex relationships and trends in data, making insights more accessible and impactful for non-technical users.
   - Interactive exploration: Users can customize charts and graphs to gain deeper understanding and identify patterns.

   **Implementation:**
   - Integrate with existing data visualization libraries like Plotly or Matplotlib.
   - Allow users to specify chart types (bar, line, pie, etc.) and customize parameters based on their query.
   - Generate interactive visualizations that update dynamically as users explore their data.

2. **Semantic Layer for Document-based Data:**

   **Benefits:**
   - Query unstructured data: Access and analyze information from documents, emails, reports, and other text-based sources.
   - Improved accuracy: Semantic understanding allows ChatDB to interpret the meaning and context of text data, leading to more precise query results.

   **Implementation:**
   - Utilize natural language processing (NLP) techniques like named entity recognition and sentiment analysis.
   - Build a knowledge graph to represent relationships between entities and concepts within documents.
   - Allow users to ask questions about specific entities, topics, or relationships within documents.

3. **Broadening Contextual Domain to the Internet:**

   **Benefits:**
   - Access external knowledge: Leverage information from the internet to enrich data analysis and provide more comprehensive insights.
   - Stay up-to-date: Access real-time data and news to gain context and understand how external factors impact internal data.

   **Implementation:**
   - Integrate with search engines and APIs to access publicly available data.
   - Develop fact-checking and verification mechanisms to ensure the accuracy and reliability of external information.
   - Allow users to specify the scope of their queries (internal data only, include external data, etc.).
