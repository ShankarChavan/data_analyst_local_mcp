# MCP Local Data Analyst

Talk to your data smoothly 💬📊. An AI Data Analyst built with the Model Context Protocol (MCP), OpenAI API, and SQLite. Turn natural language into SQL queries. Includes a Dockerized Streamlit UI.

## Getting Started

### Prerequisites

Before running the application, make sure you have the following installed:

1. **Python 3.9+** - For local development
   - Download from [python.org](https://www.python.org/downloads/)

2. **Docker & Docker Compose** (optional) - For containerized deployment
   - Install Docker Desktop from [docker.com](https://www.docker.com/products/docker-desktop)
   - Includes Docker Compose by default

3. **OpenAI API Key** - For using OpenAI's models
   - Get an API key from [OpenAI Platform](https://platform.openai.com/api-keys)

### Installation & Running Locally

1. Clone the repository

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Set your OpenAI API key as an environment variable:
   ```bash
   export OPENAI_API_KEY="your-api-key-here"
   ```

4. Run the Streamlit app:
   ```bash
   streamlit run src/app.py
   ```

5. Open your browser and navigate to:
   ```
   http://localhost:8501
   ```

### Running with Docker

1. Set your OpenAI API key in your environment or `.env` file

2. Start the application with Docker Compose:
   ```bash
   docker-compose up --build
   ```

3. Open your browser and navigate to:
   ```
   http://localhost:8501
   ```

### Testing the MCP Server

To test the MCP server independently using the MCP Inspector web tool:

```bash
npx @modelcontextprotocol/inspector python src/server.py
```

This opens an interactive web UI at `http://localhost:5173` where you can:
- Inspect the database schema
- Test the `query_database` tool
- Debug SQL queries in real-time

### Configuration

- Modify the database by editing `src/seed_data.py` if needed
- Configure model selection and API key in the Streamlit UI
- Data is stored in the `data/` directory

