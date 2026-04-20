# Text2SQL-ai-agent

A proof-of-concept Text-to-SQL agent that uses an LLM to generate and execute MySQL queries against a local database.

## Overview

This repository contains a Jupyter notebook, `Text2SQL_Agent.ipynb`, which demonstrates:

- provisioning a local MySQL database
- loading the BIRD SQL dataset
- building a tool-enabled Text2SQL agent persona
- generating step-by-step plans and SQL queries with an LLM
- listing tables, inspecting schemas, and executing read-only queries

## Contents

- `Text2SQL_Agent.ipynb` - interactive notebook with setup, prompt construction, and example query execution.

## Setup

1. Install dependencies in your Python environment.

   - If using pip:
     ```bash
     pip install mysql-connector-python sqlalchemy datasets openai
     ```

2. Ensure MySQL is installed and running locally.
3. Update notebook credentials if your MySQL setup is different from the default:
   - host: `localhost`
   - port: `3306`
   - user: `root`
   - password: `root`

## Usage

1. Open `Text2SQL_Agent.ipynb` in Jupyter or VS Code.
2. Run the notebook cells sequentially to:
   - install and start MySQL
   - create the `BIRD` database
   - load sample data
   - define agent prompts and query tools
   - generate and execute SQL queries via the LLM

## Notes

- The notebook is designed for read-only SQL operations.
- It shows a safe workflow for building Text2SQL tools, including schema inspection and query validation.
- The current example uses `gpt-4o-mini` through the OpenAI Python client.

## License

Use and modify this project as needed.
