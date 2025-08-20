# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a LangChain learning repository containing fundamental examples and tutorials. The project demonstrates basic LangChain concepts including chat models, prompt templates, and AI model integrations.

## Development Setup

### Environment Setup
```bash
# Create and activate virtual environment
python3 -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# Set up environment variables
cp .env.example .env
# Edit .env to add your actual API keys for GOOGLE_API_KEY and OPENAI_API_KEY
```

### Running Examples
```bash
# Activate virtual environment first
source venv/bin/activate

# Run individual examples
python 1-fundamentos/1-hello-world.py
python 1-fundamentos/2-init-chat-model.py
python 1-fundamentos/3-prompt-template.py
python 1-fundamentos/4-chat-prompt-template.py
```

## Architecture

### Project Structure
- `1-fundamentos/` - Contains fundamental LangChain examples
  - Basic chat model usage with OpenAI and Google models
  - Prompt template examples
  - Chat prompt template demonstrations
- `venv/` - Python virtual environment (should not be modified)
- `requirements.txt` - Python dependencies
- `.env` - Environment variables (API keys)

### Key Dependencies
- **langchain**: Core LangChain framework
- **langchain-openai**: OpenAI model integration
- **langchain-google-genai**: Google Generative AI integration
- **python-dotenv**: Environment variable management

### Model Integration
The codebase demonstrates two main AI providers:
- OpenAI models (GPT variants) via `langchain-openai.ChatOpenAI`
- Google models (Gemini) via `langchain.chat_models.init_chat_model`

### Environment Variables Required
- `OPENAI_API_KEY`: For OpenAI model access
- `GOOGLE_API_KEY`: For Google Generative AI access

## Common Patterns

- All examples load environment variables using `dotenv.load_dotenv()`
- Models are typically configured with temperature settings for response variability
- Prompt templates use input variables for dynamic content generation