# neo4j_ANLP3
# 🎬 Movie Knowledge Graph Assistant 


## 🚀 Project Overview
The application acts as an intelligent intermediary query engine that parses natural language questions about movies, actors, and directors, maps them to optimized Cypher queries, executes them against a Neo4j instance, and displays beautiful, structured results.

### 🏗️ Architecture & Flow
1. **Neo4j DB Connection**: Establishes a connection to your Neo4j Sandbox/Instance using official credentials.
2. **Natural Language Processing (Pattern Matching)**: Translates simple user questions (e.g., *"Who directed The Matrix?"*) into formal graph database query structures (Cypher).
3. **Safe Execution Boundary**: Sanitizes incoming requests to prevent query injection risks (e.g., blocking `SET`, `MERGE`, `DELETE`, `DROP`).
4. **Streamlit Application (`app.py`)**: A modern and sleek frontend with custom CSS themes built directly inside this environment.
5. **Secure Public Tunneling (pyngrok)**: Safely exposes the local Streamlit port `8501` to an external URL, allowing you to access the web application on any device.

## 🛠️ Step-by-Step Guide to Run the App

1. **Install Dependencies**: Execute the setup cells to pull down `neo4j`, `pyngrok`, and `streamlit` packages.
2. **Neo4j Configuration**: Input your unique instance's `URI`, `Username`, and `Password` when prompted by the credential manager.
3. **Write `app.py`**: The `%%writefile app.py` cell configures your custom layout and includes pre-compiled regex schemas to map queries directly to Cypher syntax.
4. **Run Streamlit**: Initialize the background process writing out outputs to a local log file.
5. **Launch Tunnel**: Generate the external HTTPS ngrok domain to share your interactive chatbot UI!
