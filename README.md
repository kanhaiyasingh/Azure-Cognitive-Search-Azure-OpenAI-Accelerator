![Azure OpenAI + Cognitive Search Accelerator](https://user-images.githubusercontent.com/113465005/226238596-cc76039e-67c2-46b6-b0bb-35d037ae66e1.png)

# Azure Cognitive Search + Azure OpenAI Accelerator

[![GitHub license](https://img.shields.io/github/license/MSUSAzureAccelerators/Azure-Cognitive-Search-Azure-OpenAI-Accelerator.svg)](https://github.com/MSUSAzureAccelerators/Azure-Cognitive-Search-Azure-OpenAI-Accelerator/blob/main/LICENSE.txt)
[![GitHub contributors](https://img.shields.io/github/contributors/MSUSAzureAccelerators/Azure-Cognitive-Search-Azure-OpenAI-Accelerator.svg)](https://github.com/MSUSAzureAccelerators/Azure-Cognitive-Search-Azure-OpenAI-Accelerator/graphs/contributors)
[![GitHub issues](https://img.shields.io/github/issues/MSUSAzureAccelerators/Azure-Cognitive-Search-Azure-OpenAI-Accelerator.svg)](https://github.com/MSUSAzureAccelerators/Azure-Cognitive-Search-Azure-OpenAI-Accelerator/issues)
[![GitHub pull-requests](https://img.shields.io/github/issues-pr/MSUSAzureAccelerators/Azure-Cognitive-Search-Azure-OpenAI-Accelerator.svg)](https://github.com/MSUSAzureAccelerators/Azure-Cognitive-Search-Azure-OpenAI-Accelerator/pull)

[![Open in GitHub Codespaces](https://github.com/codespaces/badge.svg)](https://codespaces.new/MSUSAzureAccelerators/Azure-Cognitive-Search-Azure-OpenAI-Accelerator?quickstart=1)
[![Open in VS Code Dev Containers](https://img.shields.io/static/v1?style=for-the-badge&label=Remote%20-%20Containers&message=Open&color=blue&logo=visualstudiocode)](https://vscode.dev/redirect?url=vscode://ms-vscode-remote.remote-containers/cloneInVolume?url=https://github.com/MSUSAzureAccelerators/Azure-Cognitive-Search-Azure-OpenAI-Accelerator)

**Build intelligent, multi-agent RAG systems with Azure services** - A comprehensive workshop and learning accelerator for creating enterprise-ready AI applications using Azure Cognitive Search, Azure OpenAI, and LangGraph.

---

## 📚 Table of Contents

- [🚀 Quick Start](#-quick-start)
- [🎯 Overview](#-overview)
- [✨ What You'll Build](#-what-youll-build)
- [🏗️ Architecture](#️-architecture)
- [🎓 Learning Path](#-learning-path)
- [📋 Prerequisites](#-prerequisites)
- [⚡ Installation](#-installation)
- [🔧 Configuration](#-configuration)
- [📖 Running the Notebooks](#-running-the-notebooks)
- [🌐 Demo](#-demo)
- [🚧 Troubleshooting](#-troubleshooting)
- [🤝 Contributing](#-contributing)
- [🏢 For Microsoft Employees](#-for-microsoft-employees)
- [📄 License](#-license)

---

## 🚀 Quick Start

**Want to get started immediately?** Follow these steps for a quick deployment:

1. **Fork this repository** to your GitHub account
2. **Deploy Azure infrastructure** by clicking: [![Deploy to Azure](https://aka.ms/deploytoazurebutton)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fpablomarin%2FGPT-Azure-Search-Engine%2Fmain%2Fazuredeploy.json)
3. **Deploy required models** in Azure AI Foundry: `gpt-4o`, `gpt-4o-mini`, `text-embedding-3-large`
4. **Clone your fork** to Azure ML or VS Code
5. **Configure credentials** in `credentials.env`
6. **Run the notebooks** in sequence starting with `01-Load-Data-ACogSearch.ipynb`

📍 **Need detailed instructions?** Jump to the [Installation section](#-installation).

---

## 🎯 Overview

This accelerator provides a comprehensive learning experience for building **intelligent multi-agent RAG (Retrieval-Augmented Generation) systems** using Azure services. Whether you're attending a Microsoft-led workshop or learning independently, this repository contains everything you need to create enterprise-ready AI applications.

### 🎯 Use Cases

**Workshop Format (3-5 days)**: Microsoft architects guide organizations through building a complete AI system with hands-on labs and business-specific customization.

**Self-Paced Learning**: Developers and data scientists can work through the notebooks independently to learn RAG patterns, multi-agent architectures, and Azure AI services integration.

**Enterprise POC**: Use this as a foundation for building production-ready intelligent document search and Q&A systems for your organization.

### 🌟 Key Features

- **100% Python** - No complex toolchains required
- **Multi-Agent Architecture** - Built with LangGraph for sophisticated agent workflows  
- **Hybrid Search** - Combines text and vector search for optimal results
- **Multi-Modal** - Supports text, audio, and image inputs/outputs
- **Multi-Lingual** - Processes documents and queries in any language
- **Production Ready** - Includes FastAPI backend and Streamlit frontend
- **Azure Native** - Leverages Azure Cognitive Search, OpenAI, CosmosDB, and more

---

## ✨ What You'll Build

By completing this accelerator, you'll have built a comprehensive **Generative AI Multi-Agent Architecture** that includes:

### 🔗 **Scalable Backend Systems**
- **Bot Framework Integration**: Connect to Microsoft Teams, SMS, Email, Slack, and more
- **FastAPI Server**: High-performance API with streaming capabilities  
- **Multi-Agent Architecture**: Intelligent routing between different data sources and capabilities

### 🖥️ **User-Friendly Frontend Applications**  
- **Web Search Interface**: Intelligent document search with source citations
- **Conversational Bot UI**: ChatGPT-like experience for your enterprise data
- **Multi-Modal Interface**: Support for text, voice, and image interactions

### 🧠 **Intelligent Data Processing**
- **RAG Implementation**: Retrieval-Augmented Generation with multiple data sources
- **Document Intelligence**: OCR, chunking, and automated vectorization
- **Tabular Data Q&A**: Natural language queries over CSV files and SQL databases
- **Web Search Integration**: Real-time internet search capabilities
- **API Integration**: Convert natural language to API calls

### 📊 **Enterprise Features**
- **Persistent Memory**: Conversation history stored in CosmosDB
- **Security**: Single-tenant deployment with proper authentication
- **Monitoring**: Built-in logging and analytics capabilities
- **Scalability**: Cloud-native architecture ready for production

---

## 🏗️ Architecture

![Architecture Diagram](./images/GPT-Smart-Search-Architecture.jpg)

### System Flow

1. **User Query**: User asks a question through any connected channel
2. **Agent Routing**: Intelligent agent determines the best data source to use
3. **Data Sources**: Five different types of sources are available:
   - **🗃️ Azure SQL Database**: COVID-related statistics and structured data
   - **🔌 API Endpoints**: RESTful OpenAPI 3.0 integrations (currency data, etc.)
   - **🌐 Web Search**: Real-time internet search via SerpAPI
   - **📚 Azure AI Search**: AI-enriched documents including:
     - TV show transcripts (FRIENDS episodes)
     - 90,000+ COVID research abstracts  
     - Complex PDF documents
   - **📊 CSV/Tabular Data**: Structured data files with natural language queries
4. **Response Generation**: Agent retrieves relevant information and crafts contextual answers
5. **Memory Storage**: Conversation state persisted in CosmosDB for context and analysis
6. **Delivery**: Response delivered with sources and explanations

### Technology Stack

| Component | Technology | Purpose |
|-----------|------------|---------|
| **Frontend** | Streamlit | Web UI for search and chat |
| **Backend API** | FastAPI | High-performance API with streaming |
| **Bot Framework** | Azure Bot Service | Multi-channel bot deployment |
| **Search** | Azure Cognitive Search | Hybrid text + vector search |
| **LLM** | Azure OpenAI (GPT-4o) | Language model and embeddings |
| **Memory** | Azure CosmosDB | Conversation persistence |
| **Documents** | Azure Document Intelligence | OCR and document parsing |
| **Storage** | Azure Blob Storage | Document and media storage |
| **Orchestration** | LangGraph | Multi-agent workflow management |

---

## 🎓 Learning Path

The accelerator is designed as a progressive learning experience through Jupyter notebooks. Each notebook builds upon the previous ones:

### 📚 **Foundation (Notebooks 1-4)**
- **01-Load-Data-ACogSearch** - Index documents and create search indexes
- **02-LoadCSVOneToMany-ACogSearch** - Handle structured data and relationships  
- **03-Quering-AOpenAI** - Basic Azure OpenAI integration and prompting
- **04-Complex-Docs** - Advanced document processing with Azure Document Intelligence

### 🧠 **RAG and Memory (Notebooks 5-6)**
- **05-Adding_Memory** - Implement conversation memory with CosmosDB
- **06-First-RAG** - Build your first Retrieval-Augmented Generation system

### 🔍 **Data Sources (Notebooks 7-10)**
- **07-TabularDataQA** - Natural language queries over CSV data
- **08-SQLDB_QA** - Database integration and SQL generation
- **09-BingChatClone** & **09-WebSearch_QA** - Web search integration
- **10-API-Search** - API integration and natural language to API calls

### 🎭 **Advanced Features (Notebooks 11-12)**
- **11-Adding_Multi-modality** - Voice, audio, and image capabilities
- **12-Smart_Agent** - Multi-agent architecture with LangGraph

### 🚀 **Deployment (Notebooks 13-15)**
- **13-Building-Apps** - Frontend development with Streamlit
- **14-BotService-API** - Bot Framework integration and deployment
- **15-FastAPI-API** - FastAPI backend with streaming capabilities

> 💡 **Tip**: Each notebook includes detailed explanations, code examples, and exercises. Allow 30-45 minutes per notebook for a thorough understanding.

---

## 📋 Prerequisites

### 💰 **Azure Requirements**
- **Azure Subscription** with contributor access
- **Azure OpenAI Service** deployed in [Azure AI Foundry](https://ai.azure.com)
- **Resource Group** for workshop resources (contributor permissions required)
- **Sufficient Quota** for Azure services (see quota requirements below)

### 🤖 **Required AI Models**
Deploy these models in your Azure OpenAI service:
- `gpt-4o` (or `gpt-4`) - Main reasoning model
- `gpt-4o-mini` (or `gpt-4-mini`) - Fast responses and function calling  
- `gpt-4o-audio-preview` - Audio processing capabilities
- `gpt-4o-realtime-preview` - Real-time audio interactions
- `text-embedding-3-large` - Document embeddings

### 🏗️ **Development Environment**
Choose one of the following:

**Option A: Azure Machine Learning (Recommended)**
- Azure ML Workspace deployed in your resource group
- Compute instance with sufficient cores (Standard_DS3_v2 or higher)
- Python 3.12 conda environment

**Option B: Local Development**
- Visual Studio Code with Python extension
- Python 3.12 or higher
- Git for repository cloning

**Option C: GitHub Codespaces**
- GitHub account with Codespaces access
- Click the Codespaces badge above for instant setup

### 📊 **Azure Service Quotas**
Ensure you have sufficient quota for:
- **Azure OpenAI**: GPT-4 and embedding model deployments
- **Azure Cognitive Search**: Basic tier or higher
- **Azure App Service**: Basic tier for hosting applications  
- **Azure CosmosDB**: Basic tier for conversation storage
- **Azure Storage**: Standard tier for document storage

### 🏢 **For Microsoft Workshops**
Additional requirements for customer-led workshops:
- Microsoft team members added as guests in customer Azure AD
- Single-tenant App Registration created by customer
- 10-20 business-specific questions prepared for testing
- Customer documents uploaded to blob storage 2 weeks prior

---

## ⚡ Installation

### **Step 1: Fork the Repository**
Fork this repository to your GitHub account to track your progress and customize as needed.

### **Step 2: Deploy Azure Infrastructure**

**⚠️ Important**: If this is your first time creating an **Azure AI Services Multi-Service Account**:
1. Manually create the account in Azure Portal
2. Read and accept the **Responsible AI Terms**  
3. Delete the manually created account
4. Then proceed with the automated deployment below

Click to deploy all required Azure services:

[![Deploy to Azure](https://aka.ms/deploytoazurebutton)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fpablomarin%2FGPT-Azure-Search-Engine%2Fmain%2Fazuredeploy.json)

This deployment creates:
- Azure Cognitive Search service
- Azure Storage account with blob containers
- Azure Cognitive Services multi-service account
- Azure Document Intelligence service
- Azure CosmosDB account
- Azure App Service plans

### **Step 3: Set Up Development Environment**

Choose your preferred development environment:

#### **🎯 Option A: Azure Machine Learning (Recommended)**

1. **Clone your forked repository** to your AML Compute Instance
2. **Create and activate conda environment**:
   ```bash
   conda create -n RAGAgents python=3.12
   conda activate RAGAgents
   pip install -r ./common/requirements.txt
   conda install ipykernel
   python -m ipykernel install --user --name=RAGAgents --display-name "RAGAgents (Python 3.12)"
   ```

#### **🖥️ Option B: Visual Studio Code**

1. **Clone your forked repository** locally
2. **Create Python virtual environment**:
   ```bash
   python -m venv .venv
   .venv\Scripts\activate  # Windows
   source .venv/bin/activate  # Linux/Mac
   pip install -r ./common/requirements.txt
   pip install ipykernel
   ```

#### **☁️ Option C: GitHub Codespaces**

Click the Codespaces badge at the top of this README for instant setup with all dependencies pre-installed.

---

## 🔧 Configuration

### **Configure Azure Service Credentials**

1. **Copy the credentials template**:
   ```bash
   cp credentials.env credentials.env.backup  # Keep a backup
   ```

2. **Edit `credentials.env`** with your Azure service values:

   ```bash
   # Azure OpenAI Configuration
   AZURE_OPENAI_ENDPOINT="https://your-openai-service.openai.azure.com/"
   AZURE_OPENAI_API_KEY="your-api-key-here"
   GPT4o_DEPLOYMENT_NAME="gpt-4o"
   GPT4oMINI_DEPLOYMENT_NAME="gpt-4o-mini"
   EMBEDDING_DEPLOYMENT_NAME="text-embedding-3-large"
   
   # Azure Cognitive Search
   AZURE_SEARCH_ENDPOINT="https://your-search-service.search.windows.net"
   AZURE_SEARCH_KEY="your-admin-key-here"
   
   # Azure Storage
   BASE_CONTAINER_URL="https://yourstorageaccount.blob.core.windows.net/"
   BLOB_CONNECTION_STRING="DefaultEndpointsProtocol=https;AccountName=..."
   BLOB_SAS_TOKEN="?sv=2022-11-02&ss=bfqt&srt=sco&sp=..."
   
   # Additional Azure Services
   AZURE_COSMOSDB_ENDPOINT="https://your-cosmosdb.documents.azure.com:443/"
   AZURE_COSMOSDB_KEY="your-cosmosdb-key"
   FORM_RECOGNIZER_ENDPOINT="https://your-doc-intelligence.cognitiveservices.azure.com/"
   FORM_RECOGNIZER_KEY="your-doc-intelligence-key"
   ```

3. **Get the required values** from Azure Portal:
   - **BLOB_SAS_TOKEN**: Storage Account → Security + networking → Shared Access Signature → Generate SAS
   - **AZURE_SEARCH_KEY**: Use the **Admin Key**, not the Query Key
   - **Other values**: Available in the respective service overview pages

### **Optional Configurations**

#### **🔍 Web Search (SerpAPI)**
For web search capabilities (Notebooks 9-10):
```bash
SERPAPI_KEY="your-serpapi-key"  # Get from https://serpapi.com/
```

#### **🎤 Speech Services**
For audio features (Notebook 11):
```bash
AZURE_SPEECH_KEY="your-speech-service-key"
AZURE_SPEECH_REGION="your-region"
```

#### **🗄️ SQL Database**
For database integration (Notebook 8):
```bash
SQL_SERVER_NAME="your-sql-server.database.windows.net"
SQL_SERVER_DATABASE="your-database-name"
SQL_SERVER_USERNAME="your-username"
SQL_SERVER_PASSWORD="your-password"
```

---

## 📖 Running the Notebooks

### **Execution Order**
⚠️ **Important**: Execute notebooks **in sequence** as each builds upon the previous ones.

### **Kernel Selection**
- **Azure ML**: Select `RAGAgents (Python 3.12)` kernel
- **VS Code**: Select the `.venv` Python interpreter  
- **Codespaces**: Default Python kernel should work

### **Getting Started**

1. **Start with Notebook 01**: `01-Load-Data-ACogSearch.ipynb`
   - This notebook indexes the FRIENDS TV show transcripts
   - Creates your first search index
   - Takes approximately 30-45 minutes

2. **Progress through the sequence**: Each notebook includes:
   - Clear learning objectives
   - Step-by-step code explanations  
   - Practical exercises
   - Troubleshooting tips

3. **Monitor your progress**: Each notebook will:
   - Validate your configuration
   - Test connections to Azure services
   - Provide checkpoint confirmations

### **Notebook Timing Guide**
| Notebook | Estimated Time | Key Learning |
|----------|---------------|--------------|
| 01-04 | 2-3 hours | Foundation setup and document processing |
| 05-06 | 1-2 hours | RAG implementation and memory |
| 07-10 | 3-4 hours | Multiple data source integration |
| 11-12 | 2-3 hours | Advanced features and agents |
| 13-15 | 2-3 hours | Application deployment |

### **Common Issues**
- **Quota exceeded**: Check your Azure OpenAI quota limits
- **Search index errors**: Ensure search service has sufficient capacity
- **Memory errors**: Consider using smaller document chunks for large datasets
- **Authentication issues**: Verify all credentials in `credentials.env`

---

## 🌐 Demo

🚀 **Live Demo**: [https://gptsmartsearch-frontend.azurewebsites.net](https://gptsmartsearch-frontend.azurewebsites.net)

Try the live demo to see what you'll build:
- Search through FRIENDS TV show transcripts
- Ask questions about COVID research papers
- Test multi-modal capabilities with voice and images
- Experience the multi-agent architecture in action

**Sample Questions to Try:**
- "What are the funniest moments between Ross and Rachel?"
- "Find information about COVID-19 treatment effectiveness"
- "What's the current exchange rate for USD to EUR?" (API integration)
- "Search for recent news about artificial intelligence" (Web search)

---

## 🚧 Troubleshooting

### **Common Setup Issues**

#### **🔐 Authentication Errors**
```bash
# Error: Invalid authentication credentials
```
**Solution**: 
- Verify all keys in `credentials.env` are correct
- Ensure you're using **Admin Keys** for Azure Search (not Query Keys)
- Check that SAS token starts with `?`

#### **📦 Python Package Issues**
```bash
# Error: Module not found or version conflicts
```
**Solution**:
```bash
# Recreate your environment
conda deactivate
conda remove -n RAGAgents --all
conda create -n RAGAgents python=3.12
conda activate RAGAgents
pip install -r ./common/requirements.txt
```

#### **🚫 Azure Quota Limits**
```bash
# Error: Rate limit exceeded or quota exhausted
```
**Solution**:
- Check your Azure OpenAI quota in Azure Portal
- Request quota increases if needed
- Use smaller batch sizes for document processing

#### **🔍 Search Index Issues**
```bash
# Error: Index not found or search failures
```
**Solution**:
- Ensure Azure Search service is running
- Check index creation completed successfully in Notebook 01
- Verify search service has sufficient capacity

### **Private Repository Cloning**

For private repositories in Azure ML:

1. **Generate SSH key**:
   ```bash
   ssh-keygen -t ed25519 -C "your_email@example.com"
   ```

2. **Copy public key**:
   ```bash
   cat ~/.ssh/id_ed25519.pub
   ```

3. **Add to GitHub**: Settings → SSH and GPG Keys → New SSH Key

4. **Clone repository**:
   ```bash
   git clone git@github.com:YOUR-USERNAME/YOUR-REPOSITORY.git
   ```

### **🎛️ Performance Optimization**

#### **Memory Issues**
- Reduce chunk sizes in document processing
- Use streaming responses for large queries
- Process documents in smaller batches

#### **Speed Improvements**
- Use `gpt-4o-mini` for faster responses in development
- Enable Azure Search query caching
- Implement request throttling for large datasets

### **🆘 Getting Help**

1. **Check Issues**: [GitHub Issues](https://github.com/MSUSAzureAccelerators/Azure-Cognitive-Search-Azure-OpenAI-Accelerator/issues)
2. **Review Logs**: Check notebook outputs for detailed error messages
3. **Azure Portal**: Monitor your Azure services for health and quota status
4. **Community**: Join discussions in the repository

---

## 🤝 Contributing

We welcome contributions to improve this accelerator! Here's how you can help:

### **Ways to Contribute**
- 🐛 **Report bugs** through GitHub Issues
- 💡 **Suggest enhancements** for notebooks or documentation
- 📖 **Improve documentation** and tutorials
- 🔧 **Submit code improvements** via Pull Requests
- 🌍 **Add translations** for international users

### **Development Setup**
1. Fork the repository
2. Create a feature branch: `git checkout -b feature/amazing-feature`
3. Make your changes and test thoroughly
4. Commit changes: `git commit -m 'Add amazing feature'`
5. Push to branch: `git push origin feature/amazing-feature`
6. Open a Pull Request

### **Contribution Guidelines**
- Follow existing code style and conventions
- Update documentation for any new features
- Test your changes across different scenarios
- Provide clear descriptions in Pull Requests

### **Code of Conduct**
This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/).
For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or
contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions.

---

## 🏢 For Microsoft Employees

This accelerator is designed as a **customer-funded Value-Based Delivery (VBD)** workshop.

### **Workshop Information**

| **Resource** | **Description** | **Link** |
|--------------|-----------------|----------|
| **VBD SKU** | Customer Invested delivery (3-5 days) | [ESXP SKU page](https://esxp.microsoft.com/#/omexplanding/services/14486/geo/USA/details/1) |
| **CSA Accreditation** | Required training for delivery | [Link 1](https://learningplayer.microsoft.com/activity/s9261799/launch), [Link 2](https://learningplayer.microsoft.com/activity/s9264662/launch) |
| **Workshop Deck** | Introduction and agenda presentation | [PowerPoint](https://github.com/MSUSAzureAccelerators/Azure-Cognitive-Search-Azure-OpenAI-Accelerator/blob/main/Intro%20AOAI%20GPT%20Azure%20Smart%20Search%20Engine%20Accelerator.pptx) |
| **Training Video** | 2-hour CSA training recording | [Recording](https://microsoft-my.sharepoint.com/:v:/p/annagross/ETONCWUYCa5EtpmnYjYy9eABK1JV1yo49HDoYjnry1C8-A) |

### **Workshop Prerequisites**
- Customer Azure subscription with Resource Group
- Microsoft team added as guests in customer Azure AD
- Customer documents uploaded 2 weeks prior
- Single-tenant App Registration created
- 10-20 business-specific test questions prepared
- Azure ML Workspace for collaboration

---

## 📄 License

Copyright (c) Microsoft Corporation. All rights reserved.

Licensed under the MIT License. See [LICENSE](LICENSE.txt) for details.

## 🏷️ Trademarks

This project may contain trademarks or logos for projects, products, or services. Authorized use of Microsoft 
trademarks or logos is subject to and must follow 
[Microsoft's Trademark & Brand Guidelines](https://www.microsoft.com/en-us/legal/intellectualproperty/trademarks/usage/general).
Use of Microsoft trademarks or logos in modified versions of this project must not cause confusion or imply Microsoft sponsorship.
Any use of third-party trademarks or logos are subject to those third-party's policies.

---

## 📞 Support

- 📚 **Documentation**: Check this README and individual notebook instructions
- 🐛 **Issues**: [GitHub Issues](https://github.com/MSUSAzureAccelerators/Azure-Cognitive-Search-Azure-OpenAI-Accelerator/issues)
- 💬 **Discussions**: [GitHub Discussions](https://github.com/MSUSAzureAccelerators/Azure-Cognitive-Search-Azure-OpenAI-Accelerator/discussions)
- 📧 **Microsoft Support**: For official workshop inquiries, contact your CSA

---

*Made with ❤️ by the Microsoft Customer Success Team*