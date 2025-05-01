FROM ollama/ollama:0.6.5

ENV OLLAMA_MODELS="/models"
ENV OLLAMA_DEBUG=true
ENV OLLAMA_KEEP_ALIVE=-1
ENV MODEL=qwen2.5:7b
# ENV MODEL=gemma3:4b
ENV OLLAMA_CONTEXT_LENGTH=10000

RUN ollama serve & sleep 5 && ollama pull $MODEL
ENTRYPOINT ["ollama", "serve"]