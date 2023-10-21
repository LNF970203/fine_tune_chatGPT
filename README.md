# fine_tune_chatGPT

**RAG framework has much benefits when compared with fine-tuning**
  - Low cost
  - Less Effort
  - Acceptable results (May not be good much as fine tuning but it depends. And it can be controlled)

This repo represents how to use RAG architecture on youtube videoes and talk with the script of the youtube videoes to get comprehensive insights.<br>

**Third prty tools used.**
  - OpenAI API services
  - Langchain
  - Pinecone (Vector DB)
  - Youtube transcript API service

**File Structure**
  - *youtube_utils.py*: Extract video id and get transcript based on the given youtube link
  - *pinecone_utils.py*: Upload sub scripts as vectors embeddings and for semantic search
  - *upload.py*: Upload vector embeddings
  - *ask.py*: Talk with LLM with semantic research results
  - *requirements.txt*: Dependencies

**How to run**
  - Install modules using requirements.txt
  - Define API keys in pinecone_utils (DO NOT ENTER OPENAI API KEY in Github: it will be rotated)
  - Define the link in upload.py and run to save vector embeddigs
  - Use ask.py to talk with the LLM


