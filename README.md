
# LLM Resume File Assistant

A Python application that lets an LLM use filesystem tools to manage
and search dummy resumes. It uses OpenRouter through the OpenAI SDK.

## Features

- Read PDF, TXT and DOCX resumes
- List files with metadata and extension filtering
- Write files and create missing directories
- Search case-insensitively with surrounding context
- Use LLM function calling to select and execute tools

## Setup

Python 3.10 or newer is recommended.

Install dependencies:

    pip install -r requirements.txt

Set your OpenRouter API key as an environment variable.

Windows PowerShell:

    $env:OPENROUTER_API_KEY="YOUR_KEY"

Optional model selection:

    $env:OPENROUTER_MODEL="openrouter/free"

Run the application from the project root:

    python llm_file_assistant.py

## Example prompts

- List files in sample_data/resumes
- Find resumes mentioning Python in sample_data/resumes
- Read sample_data/resumes/john_doe.txt and save a summary to
  output/john_doe_summary.txt

## Project structure

- fs_tools.py: filesystem operations
- llm_file_assistant.py: LLM tool-calling application
- requirements.txt: dependencies
- sample_data/resumes/: fictional resume files
- output/: generated summaries

## Security

Use fictional or authorized files only. Never commit API keys.
Check destination paths before allowing files to be overwritten.

## Demo

Record a 2-3 minute video showing filesystem tests, LLM tool calls,
resume search, and generation of a summary file.
