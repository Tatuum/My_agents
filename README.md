# Personal Career AI Agent

A personal AI agent system that creates an interactive chat interface to represent and communicate on behalf of a specific person. The system uses AI to answer questions about the person's career, background, skills, and experience while maintaining a professional and engaging conversation style.

## Features

- Interactive chat interface built with Gradio
- Personalized responses based on LinkedIn profile and background summary
- Automatic recording of user interactions and questions
- Push notifications for new user engagements
- Professional conversation handling with potential clients or employers

## Prerequisites

- Python 3.12 or higher
- UV package manager
- OpenAI API key
- Pushover API credentials (for notifications)

## Installation

1. Clone the repository:
```bash
git clone https://github.com/Tatuum/My_agents.git
cd my_agents
```
2. Install UV

Follow the instructions here to install uv - I recommend using the Standalone Installer approach at the very top:

https://docs.astral.sh/uv/getting-started/installation/

3. Install dependencies and create virtual environment using UV:
```bash
uv sync
```

This will automatically create a virtual environment and install all dependencies from `pyproject.toml` and `uv.lock`.

## Configuration

1. Create a `.env` file in the project root with the following variables:

OPENAI_API_KEY=your_openai_api_key
PUSHOVER_TOKEN=your_pushover_token
PUSHOVER_USER=your_pushover_user

2. Set up your personal data:
   - Create a `me` directory in the project root if it doesn't exist
   - Export your LinkedIn profile as PDF and save it as `me/linkedin.pdf`
   - Create a `me/summary.txt` file with a comprehensive summary of your background, skills, and experience
   - The summary should be in plain text format and include key information about your career, education, and professional achievements


## Project Structure

- `app.py` - Main application file containing the chat interface and agent logic
- `me/` - Directory containing personal information
  - `linkedin.pdf` - LinkedIn profile information
  - `summary.txt` - Personal background summary
- `my_agents.ipynb` - Jupyter notebook for development and testing
- `pyproject.toml` - Project dependencies and metadata
- `uv.lock` - UV package manager lock file

## Usage

Run the application using UV:
```bash
uv run app.py
```

This will start the Gradio web interface where users can interact with the AI agent.


