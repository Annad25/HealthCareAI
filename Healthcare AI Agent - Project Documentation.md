# **Healthcare AI Agent \- Project Documentation**

## **1\. Platform Selection Rationale**

### **Why Autogen?**

Autogen was selected because:

* **Multi-Agent Collaboration**: Allows multiple agents to work together for complex tasks.  
* **LLM Integration**: Uses OpenAI’s GPT-4o-mini to process patient interactions.  
* **Modular System**: Supports workflow automation and custom tool integrations.  
* **Web and Database Connectivity**: Agents can browse the web and store/retrieve data from MongoDB.  
* **Scalability**: Can be extended with more features such as document processing.

## **2\. Architectural Diagram**

The system consists of multiple agents, each handling a specific function:

* **DoctorWebSurfer** \- Searches online for doctor availability.  
* **AssistantAgent** \- Verifies and summarizes information.  
* **UserProxyAgent** \- Acts as a fallback for user input.  
* **BookingAgent** \- Stores patient appointments in a MongoDB database.  
* **FollowUpAgent** \- Manages follow-up visits.  
* **InsuranceDetailsAssistant** \- Retrieves insurance-related details using a vector database (Pinecone).

## **3\. Secure Document Upload Handling**

* Currently, document upload is **not implemented**.  
* Future integration options:  
  * **OCR-based document processing** (e.g., Tesseract, PaddleOCR).  
  * **Autogen document processing tools**.  
  * **Secure file storage (AWS S3, Google Drive API)**.

## 

## 

## **4\. Running the AI Agent Locally**

### **Setup Instructions**

#### **Prerequisites**

* **Python 3.8+**  
* **MongoDB (for storing appointment data)**  
* **OpenAI API key**  
* **Pinecone API key (for insurance data retrieval)**  
* **Autogen studio**

#### **Installation Steps:** 

1. **Install dependencies: pip install autogen pymongo langchain-openai langchain-pinecone**

**Start Autogen Studio:**

* **In your cmd write autogenstudio ui \--port 8080**  
* **Go to the website**   
* **Click on team builder**  
* **Click on new team**  
* **Click on switch to json**  
* **Then paste the json file we have shared**   
* **Save it**   
* **Click on Run**  
* **You will need to add your openai and pinecone api key**  
* **Run the AI assistant and interact via the chat interface.**

## **5\. Deployment Plan**

**Currently, the system runs locally in Autogen Studio.**

## **6\. Future Enhancements**

* **Implement secure document upload with OCR.**  
* **Deploy a cloud-hosted version.**  
* **Improve error handling and multi-turn dialogues.**  
* **Add voice-based interaction support.**

