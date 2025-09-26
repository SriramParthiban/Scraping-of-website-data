# Scraping-of-website-data

# Automated User Query Scraper Workflow (n8n + OpenAI + FireCrawl)

This repository contains an **n8n workflow** that automatically extracts user queries from chat messages, processes them, scrapes relevant URLs for plain text content, aggregates the results, and formats them for output using AI models.

---

## Workflow Overview

The workflow follows these steps:

1. **When chat message received**  
   Triggers the workflow whenever a new chat message is received.

2. **Extract User Queries**  
   Uses OpenAI (via OpenRouter GPT) to identify and extract queries from the received chat message.

3. **Auto-fixing Output Parser**  
   Ensures the extracted output is correctly structured and formatted for downstream processing.

4. **Structured Output Parser**  
   Converts parsed data into a structured format for better handling in the workflow.

5. **Split Out Queries**  
   Splits multiple queries into individual items for iterative processing.

6. **Loop Over Items**  
   Iterates over each query item.

7. **Scrape URL using Plain Text**  
   Scrapes the content of the URLs associated with the queries in plain text format.  
   *(Uses FireCrawl API: `https://api.firecrawl.dev`)*

8. **Aggregate**  
   Combines all scraped content into a single dataset for further processing.

9. **Format**  
   Formats the aggregated results using OpenAI to generate human-readable outputs.

---

## Key Features

- Automated extraction of queries from chat messages.
- Intelligent parsing and error-fixing of output.
- Iterative processing of multiple queries.
- URL scraping with plain text content retrieval.
- Aggregation and formatting of results using AI models.

---

## Technologies Used

- **n8n**: Workflow automation tool.
- **OpenRouter GPT / OpenAI**: NLP for query extraction and formatting.
- **FireCrawl API**: Web scraping and content extraction.
- **Structured Output Parsers**: Ensures data integrity and correct formatting.

---

## Future Improvements

- Support for multiple scraping formats (HTML, JSON, PDF).  
- Advanced AI summarization of scraped content.  
- Integration with additional chat platforms and messaging services.  

---

## Usage

1. Import the workflow into your **n8n instance**.  
2. Set up the **OpenAI / OpenRouter API credentials**.  
3. Configure **FireCrawl API credentials**.  
4. Trigger the workflow by sending a chat message.  
5. View the aggregated and formatted output.

---

## Author

**Sriram Parthiban**  
GitHub: [YourGitHubUsername](https://github.com/YourGitHubUsername)

