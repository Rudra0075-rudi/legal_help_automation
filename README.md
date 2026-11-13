# AI Legal Research Assistant

An n8n workflow that accepts a legal question and country from a web interface, gathers source material and returns a structured response.

## Included here
- [legal-research-workflow.json](legal-research-workflow.json): the backend workflow export
- [demo-links.md](demo-links.md): the existing Lovable demo and screenshot links

The Lovable front-end source is not included in this repository.

## Workflow
1. Receive a request through a webhook.
2. Use an OpenAI model to research the question.
3. Retrieve page content through an HTTP scraping step.
4. Extract relevant information.
5. Return a response to the caller.

## Technology
n8n, OpenAI, Firecrawl and a Lovable interface.

## Setup
1. Import the JSON file into n8n.
2. Configure your own OpenAI and scraping-service credentials.
3. Inspect the webhook input mapping and connect it to your front end.
4. Test with the n8n test webhook before enabling the production endpoint.
5. Review the sources and response before relying on the output.

## Limitations
This is a research prototype, not a substitute for a qualified lawyer. A source link alone does not prove an answer is correct or current. Verify jurisdiction, source dates and quoted legal provisions.

**Author:** Rudra Joyti Maitra Soham
