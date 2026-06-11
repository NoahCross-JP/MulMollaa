# MulMollaa
MulMollaa is a local application that integrates with Ollama / llama-server, enabling multiple LLMs to converse with each other.  
All conversation flow is controlled entirely through prompts, and multiple agents can be managed using the concept of “units” (similar to meeting rooms).

> Note: The Python version is closed-source and not publicly available.  
> Only the EXE version is released.

---

## Features
- Unlimited multi-LLM conversations  
- Full conversation control via prompts  
- Web-based UI  
- Uses the Ollama / llama-server API  
- Automatically generates user data on first launch  
- Distributed as a single EXE file (Nuitka onefile)

---

## System Requirements
- **OS:** Windows 11  
- **Required:**  
  - Ollama or llama-server running locally  
  - A model must be loaded  
- **Python version:** Closed-source and not publicly available

---

## How to Use

### 1. Preparation
Before launching MulMollaa, start one of the following locally:

- **Ollama**
- **llama-server**
- Or both

The API must be active.

---

### 2. Launch
When you double-click the EXE, the following actions occur automatically:

- Console window opens  
- Browser launches  
- Files are extracted to the TEMP folder  
- A `.mulmollaa` folder is created in the user profile  
  - Configuration files  
  - Prompt files  

---

## Using AI Chat
Prefix the configured LLM name with a **half-width @** to call it.

Example:
@main Do you think Tokugawa Ieyasu had his sights set on unifying Japan from the beginning?


*Note: Add a half-width space after the name.*

---

## LLM Configuration Items
name              : Arbitrary name
node              : Ollama or llama
history-limit     : Number of past messages to remember
connection        : API endpoint URL
loadmodels-model  : Model specification for Ollama
modelfile         : Model specification for llama
vision            : Not supported yet
unitname          : Concept similar to a meeting room
prompt            : System prompt


### Example: API Endpoint URLs
llama   http://localhost:8080/v1/chat/completions
Ollama  http://localhost:11434/api/generate


---

## Unit Settings
A unit represents a “meeting room.”  
Currently, the following items are mainly used:

- `unitname` (unit name)  
- `order` (display order)  

Other items will be added in future updates.

---

## Notes
- **UTF-8N** encoding is recommended  
- Security measures are not yet implemented  
- No external communication other than LLM API requests  
- Python version is closed-source and not available  

---

## License
This project is planned to use a **Proprietary License / EULA**.  
The code is not yet in a state that can be shown publicly.

---

## Future Development (Roadmap)
MulMollaa is still under active development, with the following features planned:

- **Shared System Prompt**
  - Unified role settings for LLMs within a unit
  - Prompt input assistance

- **LLM Enable/Disable Settings**
  - Toggle LLMs on/off from the chat UI

- **Unit-Based Workflow UI**
  - Visual editing of connections between units and routing

- **Function Calling Support**
  - External function invocation via LLMs (Skills)

- **Vision Support (Image Input)**
  - Send images to LLMs for analysis

- **Autonomous Learning Loop**
  - Self-learning from inputs, outputs, and generated data

- **UI Upgrades**
  - Improved chat UI
  - Dark mode
  - Layout enhancements

- **Log Management**
  - Save and load conversation logs

*Note: The above items are subject to change.*

