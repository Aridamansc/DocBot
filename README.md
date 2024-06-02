# DocBot: A Multi-Modal Question-Answering System for PDFs

## Problem Statement
The DocBot challenge aims to develop an intelligent chatbot-based assistance system capable of efficiently processing documents containing text,tables and images. Participants are required to create a user-friendly interface allowing users to input documents and interact with the chatbot to seek information related to the document content. Upon receiving queries, the chatbot should retrieve or generate meaningful textual answers along with the most relevant image(s) and table(s) from the document, specifying the corresponding page number(s) where they are located.

## Approach
The project utilizes a multi-modal Retrieval Augmented System (RAG) and the LangChain framework to enhance the user experience and accessibility of multimodal PDFs. The pipeline involves the following steps:

1. Use a multimodal LLM (such as Claude Opus 3 and LLaVA) to produce text summaries from images.
2. Embed and retrieve image summaries with a reference to the raw image.
3. Pass raw images and text chunks to a multimodal LLM for answer synthesis.
4. Use Unstructured to parse images, text, and tables from documents (PDFs).
5. Use OpenClip embeddings for extracting image embeddings from the image space.
6. Utilize a multi-vector retriever with Chroma/Mongo to load/store raw text, tables, and images along with their summaries for retrieval.

## Multi-Functionality
- Capable of handling complex composite queries across various PDFs.
- Provides output on a Chain of Thought basis, which is visible to the user.
- Can provide query-relevant images/tables.
- Capable of handling inputs/outputs in both Japanese and English, with easy toggling.
- Can dynamically create tools for different PDFs.
- Incorporated with various LLM tools such as math, human tool, etc.
- Text-to-voice and voice-to-text capabilities.

## Accessibility Impact
The integration of the Retrieval Augmented System and LangChain Framework has a profound impact on document accessibility, especially for users with diverse needs. This technology empowers inclusive access to information.

## Prerequisites
- Python 3.10 or later
- pip package installer
- PyTorch (with CUDA support) if using Windows (installation instructions on PyTorch's official website)

## Installation
# Installation
1. Clone the repository: `git clone <repository_url>`
2. Navigate to the cloned repository directory: `cd <repository_name>`
3. Install the required packages: `pip install -r requirements.txt`
   
## Running the Application
1. Ensure you have the necessary prerequisites installed. See Important Notes.
2. Start the Streamlit app: `streamlit run streamlit.py`


