


<!-- This is the markdown template for the final project of the Building AI course, 
created by Reaktor Innovations and University of Helsinki. 
Copy the template, paste it to your GitHub README and edit! -->

# Project Title

Rag-Chat: AI-Powered Conversational Documentation Assistant

## Summary

An intelligent documentation search system that uses Azure OpenAI and RAG (Retrieval Augmented Generation) to help users find relevant information in company documentation through natural language conversations. The system provides accurate, context-aware responses by combining Azure AI Search with custom-instructed AI assistants, making technical documentation more accessible and user-friendly.


## Background

This solution addresses several common challenges in technical documentation:

* Users often struggle to find specific information in large documentation repositories, leading to reduced productivity and frustration
* Technical documentation can be overwhelming for newcomers, making it difficult to understand core concepts and get started
* Traditional search methods may miss context and related information that would be helpful for the user
* Documentation queries often require multiple searches to find complete answers to complex questions

The project aims to improve the documentation experience by providing an intuitive, conversation-based interface that understands natural language queries and provides comprehensive, context-aware responses.


## How is it used?

The solution consists of a web application built with React and TypeScript, hosted on Azure, that provides a chat interface where users can:

1. Ask questions in natural language about any documented topic
2. Receive relevant answers pulled directly from official documentation
3. Get contextual explanations and related information
4. Follow up with clarifying questions while maintaining conversation context

The system is particularly valuable in these situations:
- New employees onboarding and learning company systems
- Developers looking for specific technical implementation details
- Users troubleshooting issues or seeking best practices
- Team members trying to understand complex workflows

Example chat interface:
![Example chat](/rag_doc_chat.png)


## Data sources and AI methods
The system leverages several Azure services and AI methods:

| Component | Description |
| --------- | ----------- |
| DocFX Source Files | Markdown (.md) files that form the basis of the documentation, including all technical content, guides, and API documentation |
| Azure OpenAI | Powers the conversational AI capabilities and natural language understanding |
| Azure AI Search | Enables efficient retrieval of relevant documentation segments |
| RAG System | Combines retrieved information with AI generation for accurate, contextual responses |
| Custom Assistant | Specially instructed AI model that ensures responses align with documentation |


The documentation pipeline:
1. DocFX generates the documentation site from markdown source files
2. The RAG system processes these markdown files to create searchable indexes
3. Azure AI Search maintains these indexes for quick retrieval
4. When a user query comes in, the system:
   - Searches the indexed documentation
   - Retrieves relevant markdown content
   - Uses Azure OpenAI to generate natural language responses based on the retrieved content

The primary data sources are:
* Markdown (.md) files from the DocFX documentation system
* Technical guides and API documentation in markdown format
* Code examples and snippets embedded in the documentation

## Challenges

Important limitations and considerations include:

* The system is only as good as the documentation it's trained on - gaps in documentation will result in gaps in answers
* While the system can provide information, it cannot replace human expertise for complex problem-solving
* Regular updates to the documentation require reindexing and potentially retraining
* The system needs careful monitoring to ensure responses remain accurate and aligned with current practices
* Privacy and security considerations when dealing with internal documentation

## What next?

Potential future enhancements include:

* Implementing multi-language support for global teams
* Adding document contribution suggestions based on common user queries
* Integrating with ticketing systems to automatically suggest relevant documentation
* Developing analytics to identify documentation gaps and improvement areas
* Adding visual and interactive elements to enhance understanding


## Acknowledgments

* Azure OpenAI and AI Search documentation
* React and TypeScript communities
* RAG system implementation best practices
* Internal development and documentation teams

The project follows all necessary compliance and security guidelines for handling internal documentation and uses Azure services in accordance with their terms of service.
