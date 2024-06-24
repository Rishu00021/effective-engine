# effective-engine

# RAG_Key

# Pinecone_Key

!pip install -qU \
    langchain==0.0.354 \
    openai==1.6.1 \
    datasets==2.10.1 \
    pinecone-client==3.1.0 \
    tiktoken==0.5.2

import os
from langchain.chat_models import ChatOpenAI

os.environ["OPENAI_API_KEY"] = os.getenv("OPENAI_API_KEY") or "YOUR_API_KEY"

chat = ChatOpenAI(
    openai_api_key=os.environ["OPENAI_API_KEY"],
    model='gpt-3.5-turbo'
)
