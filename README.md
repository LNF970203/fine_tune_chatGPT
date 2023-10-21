# fine_tune_chatGPT

**RAG framework has much benefits when compared with fine-tuning**
  - Low cost
  - Less Effort
  - Acceptable results (May not be good much as fine tuning but it depends. And it can be controlled)

Therefore, I have used RAG here.<br>
<br>
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
  - Define youtube links in upload.py and run to save vector embeddigs in VectorDB
  - Use ask.py to talk with the LLM with most relevant content

**Process**
  - Define youtube links
  - Get the scripts
  - Seperate it to chunks (You can use any video with any duration. Since openAI has token limit, need to chunk the script)
  - Get embeddings from openAI and save inside vector DB
  - User Prompt and get relevent content from semantic search
  - With the relevent content, talk with LLM for abstractive insights

**TODO**
- Can define benchmark similarity score to get relevant content. Based on that, if the score is less than benchmark, manual prompt can be used to overcome getting unrelated content.

**IMPORTANT NOTES**
- If transcript generation is disabled for the youtube videoes that you have defined, by Youtube, full script cannot be extracted.
- This error is handled when getting the script in code base.
