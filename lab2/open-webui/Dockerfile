FROM ghcr.io/open-webui/open-webui:main

# Optional: CSS file
# Content Credit https://sliplane.io/blog/how-to-build-custom-open-webui-themes

USER root:root
USER 0:0
# Copy your custom CSS file
COPY custom.css /app/backend/open_webui/static/
COPY custom.css /app/build/static/
