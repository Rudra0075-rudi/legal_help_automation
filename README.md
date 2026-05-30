# legal_help_automation
This project is a fully automated AI-powered legal assistant application built using Lovable and N8N. The app allows users to enter a legal question and select a country. Based on the input, the system searches relevant official government websites, extracts useful legal information, and provides a clear, structured response with source links.

The main goal of this project is to make legal research faster, easier, and more accessible by combining no-code development, AI models, web search, and automated web scraping.

What the App Does

The AI Legal Assistant helps users by:

* Taking a legal question from the user
* Allowing the user to select a country
* Searching official government websites for relevant legal information
* Scraping useful content from websites, PDFs, or embedded legal documents
* Extracting the most relevant answer from the collected data
* Formatting the final response into readable legal guidance
* Sending the final answer back to the app interface

This project demonstrates how AI and automation tools can be used to build a practical legal research assistant without traditional coding.

Tools and Technologies Used

* Lovable – Used to build the front-end user interface
* N8N – Used to automate the backend workflow
* OpenAI GPT Models – Used for search, reasoning, extraction, and response formatting
* Firecrawl.dev – Used for scraping web pages and converting content into LLM-ready data
* Webhook – Used to connect Lovable with N8N
* HTTP Request Node – Used inside N8N to connect with external scraping services
* Respond to Webhook Node – Used to send the final result back to the Lovable app

How It Works

1. User Interface with Lovable

The front end of the app is created using Lovable. The interface contains a simple form where the user enters:

* A legal question
* A country from a dropdown menu

The design is dark, modern, clean, and user-friendly. After the user submits the form, Lovable sends the data to N8N through a webhook using a POST request.

2. Backend Workflow with N8N

N8N receives the submitted data through a Webhook node. The workflow captures the legal question and selected country. The data is then pinned inside N8N to make testing easier during development.

3. AI Search with OpenAI

OpenAI is used to search for relevant legal information from official government websites. The AI is instructed to focus only on reliable and official sources. It generates an initial answer and provides useful source links.

4. Web Scraping with Firecrawl.dev

Some official legal information may be inside PDFs, embedded pages, or complex websites. To handle this, Firecrawl.dev is used to scrape and convert website content into structured JSON data that can be processed by AI models.

The scraping URL and search terms are dynamically passed from the previous workflow steps, making the process automated.

5. Information Extraction

After the scraping process, an Information Extractor node is used to identify the most relevant legal information from the scraped content. This helps remove unnecessary text and keeps the answer focused on the user’s question.

6. Response Formatting

A second AI model is used to convert the extracted raw data into a clear and human-readable answer. This step improves the quality, readability, and structure of the final response.

The final output usually includes:

* Direct answer to the legal question
* Explanation in simple language
* Relevant legal context
* Source links from official websites

7. Sending the Answer Back to Lovable

The final formatted answer is sent back to the Lovable app using the Respond to Webhook node. The app then displays the response in a dedicated answer section for the user.

Key Features

* No-code AI legal assistant
* Simple and modern user interface
* Country-based legal question input
* Automated backend workflow
* AI-powered legal research
* Official government website search
* Web scraping support for complex pages and PDFs
* Structured and readable legal answers
* Source links included
* Can be expanded into a SaaS product

This project shows how no-code tools and AI can be combined to create a practical legal assistant app. By using Lovable for the front end, N8N for automation, OpenAI for legal reasoning, and Firecrawl.dev for web scraping, the system can collect, process, and present legal information in a fast and user-friendly way.
The project can be further developed into a full legal-tech SaaS product for law firms, legal researchers, and public users.
