PREREQUISITES:
    Python (Version 3.9 - 3.10)

ENVIRONMENT SETUP:
    1. Create a virtual environment (python -m venv .venv || python3.10 -m venv .venv)
    2. Activate the virtual environment (mac: source .venv/bin/activate)
    3. Install google-adk (pip install google-adk==0.1.0)

TYPES OF WORKFLOWS:
    1. LLM Agent: Picks one agent that fits best to answer the prompt
    2. Loop Agent: Iterates between scriptwriter, visualizer, and formatter agent. Maximum iteration is 3.

RUNNING THE AGENT:
    CONNECT TO A VPN BEFORE RUNNING. List of countries where Gemini API is available: https://ai.google.dev/gemini-api/docs/available-regions#available_regions
    I. THROUGH TERMINAL
        1. Open terminal and navigate to 'ai-agents'
        2. Run the command 'adk run youtube-shorts-assistant'
        3. Type the prompt
        4. Input 'exit' to exit
    II. THROUGH WEB
        1. Open terminal and navigate to 'ai-agents'
        2. Run the command 'adk web'
        3. Open 'http://localhost:8000' or 'http://0.0.0.0:8000' in an internet browser
        4. Type in prompt
        5. Press (CTRL + C) to quit
    III. PROGRAMATICALLY
        1. Uncomment line 82-119 in agent.py
        2. Type in the desired prompt in line 119 of agent.py
        3. Open terminal and navigate to 'ai-agents'
        4. Run the command 'python youtube-shorts-assistant/agent.py'

COMMON BUGS:
    1. An unsolved bug from gemini disallows users to add tools to LlmAgents directly, a workaround of this bug can be seen in 'agent.py' line 22-29 in the variable 'Agent_Search'. This agent is then used as a AgentTool in the scriptwriter_agent.

TESTING IF AGENT IS WORKING
Try inputting any prompts to the agent to know if the agent returns any errors.

