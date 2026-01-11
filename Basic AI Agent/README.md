# Basic AI Agent – n8n Workflow

This workflow creates an interactive AI agent with a public chat interface. The agent uses Google Gemini to respond to user questions, access real-time weather data, and fetch news from RSS feeds while remembering conversation context.

## What the workflow does
1. Receives messages through a public chat interface.
2. Processes user input with conversation memory (last 30 messages).
3. Uses Google Gemini to understand requests and select appropriate tools.
4. Fetches real-time weather data or latest news when needed.
5. Responds conversationally with relevant information.
6. Can be activated and shared via public URL.

## Main components
- Sticky Notes: Explain workflow functionality and setup steps.
- Example Chat: Public chat trigger for user interaction.
- Your First AI Agent: Core agent that orchestrates conversation and tool usage.
- Connect Gemini: Google Gemini AI model (temperature set to 0).
- Conversation Memory: Remembers last 30 messages for context.
- Get Weather: HTTP tool for weather forecasts via Open-Meteo API.
- Get News: RSS feed reader for multiple news sources.

## Setup
### Configure Google Gemini API
1. Visit [Google AI Studio](https://aistudio.google.com/app/apikey)
2. Click "Create API key in new project"
3. Copy the API key
4. Open the Connect Gemini node
5. Select Credential → Create New
6. Paste API key and save

### Activate the workflow
1. Click the Activate toggle in n8n
2. Share the public chat URL with users

## Customization
### Change agent personality
Edit the "Your First AI Agent" node:
- Modify the System Message to adjust behavior, tone, and instructions

### Add more tools
Click ➕ under the agent's Tool input:
- Add Google Calendar (Get Upcoming Events)
- Add Gmail (Send an Email)
- Add custom HTTP requests
- Add database queries

### Adjust memory length
Modify the "Conversation Memory" node:
- Change contextWindowLength (default: 30)

### Switch AI model
Replace the "Connect Gemini" node with another LLM:
- OpenAI
- Claude
- OpenRouter
- Ollama (local models)

### Modify tool parameters
Edit Get Weather or Get News nodes to:
- Change API endpoints
- Add/remove RSS feed sources
- Adjust weather parameters
