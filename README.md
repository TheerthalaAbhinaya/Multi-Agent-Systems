## MULTI-AGENT JOB APPLICATION ASSISTANT

This project showcases a multi-agent system developed with CrewAI, in which several intelligent agents work together to automatically create a job application (creating a cover letter and designing a resume).  To finish the activity from beginning to conclusion, each agent carries out a defined duty and interacts with others.

## OBJECTIVE

To demonstrate how a small-scale multi-agent system can work together to:
-> Extract key requirements from a job description
-> Tailor a resume to fit the job
-> Generate a custom cover letter
-> Proofread all content for clarity and correctness

## AGENTS AND RESPONSIBILITIES

Each agent is given a specific goal, and tasks are coordinated using the Crew architecture:

  **1.	Job Analyzer**
  
	~ Task: Analyze the job description and extract key skills and requirements.
	~ Tool Used: OpenAI LLM via langchain (GPT-3.5).

  **2.	Resume Tailor**
 
	~ Task: Modify the provided resume to align with job requirements identified by the Job Analyzer.
	~ Tool Used: OpenAI LLM.
	
  **3.	Cover Letter Generator**
  
	~ Task: Create a customized cover letter using the tailored resume and job description.
	~ Tool Used: OpenAI LLM.
	
  **4.	Proofreader**
  
	~	Task: Final check for grammar, tone, and structure in the resume and cover letter.
	~	Tool Used: OpenAI LLM.
 
## TOOLS USED

 **CrewAi** : for agent orchestration
 **LangChain & OpenAI** : for LLM- powered reasoning
 **Python** : as the base language

## HOW TO RUN THE CODE

**1. Open the notebook**

	•      Go to the GitHub repo(https://github.com/TheerthalaAbhinaya/Multi-Agent-Systems)
	•	Click on the .ipynb file.
	•	Click the “Open in Colab” button (or copy the GitHub file URL(https://github.com/TheerthalaAbhinaya/Multi-Agent-Systems/blob/main/multiagentjob.ipynb)and paste it into https://colab.research.google.com/ under “GitHub” tab).
 
**2.	Install Required Packages**

- At the top of the notebook, run the following code in cell:

~ !pip install crewai langchain openai

**3.	Add Your OpenAI API Key:**

- Create and run this cell before agent execution:

~ import os
os.environ["OPENAI_API_KEY"] = "your-api-key-here"

- *Replace "your-api-key-here" with your valid OpenAI API key.*

**Note: 
	•	To generate your own API Key, go to https://platform.openai.com/api-keys
	•	Login-> API Keys page-> Create new secret key-> Copy the key immediately and store it safely — you won’t be able to see it again.
	•	A valid OpenAI API key is required for the agents to function.
	•	The key must be provided every time you open a new Colab session or run locally.**
 
**4. Run the Script or Notebook**

  • Use Runtime > Run all in Colab to execute the entire notebook.
  • Otherwise, Run the notebook cells in order from top to bottom. 
  • Each cell represents a step in the multi-agent system (agent creation, task assignment, execution, etc.).
  • Follow the cell sequence to generate outputs.
  • You will see outputs from each agent under their respective tasks.


