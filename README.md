cd open_deep_research
uv venv
source .venv/bin/activate  # On Windows: .venv\Scripts\activate

uv sync # or: uv pip install -r pyproject.toml

#Set up your .env file to customize the environment variables (for model selection, search tools, and other configuration settings):
cp .env.example .env

uvx --refresh --from "langgraph-cli[inmem]" --with-editable . --python 3.11 langgraph dev --allow-blocking

- 🚀 API: http://127.0.0.1:2024
- 🎨 Studio UI: https://smith.langchain.com/studio/?baseUrl=http://127.0.0.1:2024
- 📚 API Docs: http://127.0.0.1:2024/docs
