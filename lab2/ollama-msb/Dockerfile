# Use Ollama Docker Image as the base
FROM ollama/ollama:0.34.1 AS builder

ENV APP_HOME=/home

WORKDIR $APP_HOME

#copy the start script
COPY . .

# Change the permission of the start script
RUN chmod +x pull-llm.sh

RUN ./pull-llm.sh

# Final image
FROM ollama/ollama:0.34.1

# Copy preloaded model cache
COPY --from=builder /root/.ollama /root/.ollama

# Expose Ollama port
EXPOSE 11434

# Run the Ollama server normally
CMD ["serve"]