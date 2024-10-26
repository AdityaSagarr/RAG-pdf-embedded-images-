
---

# 📖 Multimodal RAG App for PDF Context Extraction

**🔍 Overview:**  
Welcome to the RAG App! This project is designed to help users extract and understand context from complex PDFs that contain mixed data formats, including text, tables, and images. By leveraging advanced retrieval and generation techniques, the app provides insightful answers to user queries based on the extracted content.

**🛠️ Technologies Used:**  
- **Unstructured Library:** For partitioning PDF documents into raw elements like images, tables, and text.  
- **Langchain:** A framework for building applications with language models, facilitating efficient summarization and retrieval.  
- **OpenAI API:** Utilizing the powerful GPT-4 model for summarizing text and images to enhance the user experience.  
- **Chroma:** A vector store for indexing and fast retrieval of embeddings from various data types.  

**📦 Features:**  
- Extracts multiple data types (text, tables, images) from PDFs for better context understanding.  
- Summarizes extracted elements to create concise and informative content.  
- Implements a multi-vector retrieval system to quickly respond to user queries.  
- Integrates both text and image data for richer responses to inquiries.  

**⚙️ Getting Started:**  
To set up the RAG App on your local machine, follow these steps:  
1. **Clone the repository:** Get a local copy of the project by running `git clone <repository-url>`.  
2. **Install Dependencies:** Make sure to install the necessary libraries using pip:  
   ```bash
   pip install "unstructured[all-docs]" pillow pydantic lxml matplotlib langchain_core langchain_openai chromadb
   ```  
3. **Set Up Environment:** Ensure you have the required tools and libraries installed:  
   ```bash
   sudo apt-get update  
   sudo apt-get install poppler-utils libleptonica-dev tesseract-ocr libtesseract-dev python3-pil tesseract-ocr-eng tesseract-ocr-script-latn
   ```  
4. **Run the Application:** Follow the instructions in the main script to extract data from your PDFs and start querying!

**🛠️ Workflow Overview:**  
![imageedit_2_5976021923](https://github.com/user-attachments/assets/0f940523-59a5-47c8-82c5-f031495cab93)


The workflow of the RAG app consists of several key stages for extracting, summarizing, and retrieving context from PDFs with mixed data types:  
1. **PDF to raw_pdf_elements:**  
   - **Image:** Extracts images for visual context.  
   - **Table:** Isolates tables for structured data retrieval.  
   - **Text:** Extracts text content for narrative understanding.  
2. **Summary of:**  
   - **Image:** Captures essential elements of each image.  
   - **Table:** Distills key information from tables.  
   - **Text:** Summarizes extracted text for quick insights.  
3. **Creating a MultiVector Retriever:**  
   - **A.** Add to Chroma-DB category-wise: Integrates summaries and raw elements for efficient indexing.  
   - **B.** Split image or text types: Categorizes extracted data using validation functions.  
   - **C.** Context joining: Merges text and images into a cohesive message for LLM processing.  
4. **LLM Augmentation:** Enhances responses by leveraging the summarized data, providing comprehensive answers to user queries.  

**❓ Usage:**  
After running the application, you can upload your PDF files, and the RAG App will extract elements for you. Simply input your queries, and the app will return relevant summaries based on the extracted content.

## Author 🧑‍💻  
**Aditya Sagar**  
[![LinkedIn Logo](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/adityasagarr)  

--- 
