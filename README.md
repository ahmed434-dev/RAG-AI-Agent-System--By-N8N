# 🤖 RAG AI Agent System by n8n

An AI-powered Retrieval-Augmented Generation (RAG) customer support agent built with **n8n, Google Gemini, Supabase Vector Store, Telegram, and Google Drive**.

The system answers customer questions through Telegram by retrieving relevant information from documents stored in a vector database. It also automates document ingestion from Google Drive to help keep the knowledge base updated.

## 🚀 Features

- **Telegram Integration:** Receive customer messages and send automated AI-generated responses.
- **AI-Powered Responses:** Use Google Gemini to understand questions and generate answers.
- **RAG Architecture:** Retrieve relevant information from stored documents to provide context-aware responses.
- **Vector Search:** Use Supabase Vector Store to retrieve relevant document content.
- **Conversation Memory:** Maintain conversational context using chat-specific session IDs.
- **Automated Document Ingestion:** Monitor a Google Drive folder for new files and process them for the knowledge base.
- **Automated Embeddings:** Convert document content into vector representations using Google Gemini embeddings.

## 🛠️ Technologies Used

- [n8n](https://n8n.io/) — Workflow automation and integration.
- [Google Gemini](https://ai.google.dev/) — AI language model and embedding models.
- [Supabase](https://supabase.com/) — Vector storage and information retrieval.
- [Telegram Bot API](https://core.telegram.org/bots/api) — Messaging integration.
- [Google Drive](https://drive.google.com/) — Document source for knowledge-base ingestion.
- **RAG (Retrieval-Augmented Generation)** — Retrieving relevant information to support AI-generated answers.

## ⚙️ How It Works

### 1. Document Ingestion

1. The Google Drive Trigger monitors a specified folder for newly created files.
2. The Download File node downloads the new document.
3. The Default Data Loader prepares the document content for processing.
4. Google Gemini embeddings convert the document content into vector representations.
5. Supabase Vector Store stores the processed information for retrieval.

### 2. Customer Support

1. A customer sends a message to the Telegram bot.
2. The Telegram Trigger receives the incoming message.
3. The AI Agent processes the question using Google Gemini.
4. The agent retrieves relevant information from the Supabase Vector Store.
5. Conversation Memory helps maintain context using the Telegram chat ID as the session key.
6. The generated response is sent back to the customer through Telegram.

## 📋 Prerequisites

Before running the workflows, you need:

- An n8n instance.
- Google Gemini API credentials.
- A Supabase project with a properly configured vector store.
- A Telegram bot and its API credentials.
- A Google Drive account with access to the folder containing your documents.

## 📥 Import the Workflow

1. Download the workflow JSON file from this repository.
2. Open your n8n instance.
3. Select **Import from File**.
4. Choose the downloaded JSON file.
5. Configure your own credentials for Google Gemini, Supabase, Telegram, and Google Drive.
6. Select the appropriate Google Drive folder.
7. Verify that the Supabase vector store and embedding configurations are compatible.
8. Test both document ingestion and customer-support workflows.
9. Activate the workflows after confirming that everything is configured correctly.

## 🔐 Setup and Configuration

Before executing the workflows, each user must configure their own credentials and API keys.

### Google Gemini API

- Add your own API key for the Gemini Chat Model.
- Configure your own API credentials for the embeddings model.

### Telegram Bot

- Create your own Telegram bot using [BotFather](https://t.me/BotFather).
- Configure your Telegram Bot Token in n8n.
- Ensure the bot and Telegram Trigger are configured correctly.

### Google Drive

- Connect your own Google account.
- Authorize the required permissions.
- Select the folder to monitor for new documents.

### Supabase

- Create your own Supabase project.
- Configure the database connection and credentials.
- Set up the required vector store table.
- Ensure that the vector dimensions and embedding configuration are compatible.

### Important Notes

- The workflow is intended to be configured with each user's own credentials and API keys.
- Replace all required credentials with your own before executing the workflow.
- The exported workflow may require additional configuration before it can run.
- Ensure that the Supabase vector store and embedding configurations are compatible.
- Test document ingestion, retrieval, and AI responses before using the system in production.
- Verify that the AI Agent uses retrieved information appropriately when answering customer questions.
- Free-tier API usage limits may apply depending on the provider and plan.
- No company documents or personal account credentials are intended to be shared with this project.

### Security

**Never share or commit API keys, access tokens, passwords, or other sensitive credentials to a public repository.**

Before publishing the project, inspect the exported workflow and remove any exposed credentials or sensitive configuration values. If a real API key or access token has already been exposed, revoke or rotate it with the relevant provider.

## 🎯 Use Cases

- Automating customer support through Telegram.
- Answering frequently asked questions using company documents.
- Building a document-based AI assistant.
- Creating a knowledge base from Google Drive documents.
- Updating a knowledge base by automatically processing new documents.

## 👨‍💻 Author

**Ahmed Ahmed Abass Fouda**

Interested in AI Automation, AI Agents, RAG systems, and building practical automation solutions with n8n.

---

*Built with n8n, Google Gemini, Supabase, Google Drive, and Telegram.*

