CrewAI
Open source made for production
<img width="664" alt="image" src="https://github.com/user-attachments/assets/4a173813-d853-4d87-ba41-7c69fe3ada76" />


<img width="706" alt="image" src="https://github.com/user-attachments/assets/20644bbf-4868-4830-956a-75220a94aba5" />

<img width="1013" alt="image" src="https://github.com/user-attachments/assets/a1342216-63f4-4301-a1ae-85dacfb151a5" />

<img width="906" alt="image" src="https://github.com/user-attachments/assets/2d3cd7fb-51dd-4806-abee-3688fcf63791" />

After using the Agents
<img width="947" alt="image" src="https://github.com/user-attachments/assets/5cefc80c-acf2-4f6f-802b-51b412480529" />

<img width="651" alt="image" src="https://github.com/user-attachments/assets/95512fbd-609f-487f-bde5-b5aa331de43e" />

Automation is pretty simple, in Agentic AI you can have many different options 
<img width="772" alt="image" src="https://github.com/user-attachments/assets/0b6e49c2-6803-42f1-b3ab-eaf3ac17f949" />

You can now use fuzzy inputs to the AI Agent
<img width="947" alt="image" src="https://github.com/user-attachments/assets/b3a75cca-6ef8-4ab0-9efe-91ec97e55a22" />

Traditional
<img width="718" alt="image" src="https://github.com/user-attachments/assets/409c9158-7fd6-4c62-8244-4939f01a56a6" />

New - Using AI Agents, you can do research and google the visitors and then crete a sales pitch
<img width="912" alt="image" src="https://github.com/user-attachments/assets/9ffc29df-e0f2-494b-83e4-9bdd68329516" />

Using ChatGPT as an example, we get the result we wanted through iterating the prompts with chatGPT to finally end up with wht we wanted. You can use Agents for this so we do not become blockers.

Multi agent systems with specific Agents
<img width="421" alt="image" src="https://github.com/user-attachments/assets/0eb54530-ebcb-48da-87f1-eaf6c62ae465" />

<img width="376" alt="image" src="https://github.com/user-attachments/assets/ce663510-4583-4476-8753-cf983d54a4cb" />

Planner Agent
```python

planner = Agent(
    role="Content Planner",
    goal="Plan engaging and factually accurate content on {topic}",
    backstory="You're working on planning a blog article "
              "about the topic: {topic}."
              "You collect information that helps the "
              "audience learn something "
              "and make informed decisions. "
              "Your work is the basis for "
              "the Content Writer to write an article on this topic.",
    allow_delegation=False,
	verbose=True
)

```

Writer Agent

```python
writer = Agent(
    role="Content Writer",
    goal="Write insightful and factually accurate "
         "opinion piece about the topic: {topic}",
    backstory="You're working on a writing "
              "a new opinion piece about the topic: {topic}. "
              "You base your writing on the work of "
              "the Content Planner, who provides an outline "
              "and relevant context about the topic. "
              "You follow the main objectives and "
              "direction of the outline, "
              "as provide by the Content Planner. "
              "You also provide objective and impartial insights "
              "and back them up with information "
              "provide by the Content Planner. "
              "You acknowledge in your opinion piece "
              "when your statements are opinions "
              "as opposed to objective statements.",
    allow_delegation=False,
    verbose=True
)
```

Write Task
```python
write = Task(
    description=(
        "1. Use the content plan to craft a compelling "
            "blog post on {topic}.\n"
        "2. Incorporate SEO keywords naturally.\n"
		"3. Sections/Subtitles are properly named "
            "in an engaging manner.\n"
        "4. Ensure the post is structured with an "
            "engaging introduction, insightful body, "
            "and a summarizing conclusion.\n"
        "5. Proofread for grammatical errors and "
            "alignment with the brand's voice.\n"
    ),
    expected_output="A well-written blog post "
        "in markdown format, ready for publication, "
        "each section should have 2 or 3 paragraphs.",
    agent=writer,
)
```

Creating the Crew

```python
crew = Crew(
    agents=[planner, writer, editor],
    tasks=[plan, write, edit],
    verbose=2
)
```

<img width="444" alt="image" src="https://github.com/user-attachments/assets/0f692d97-2373-463d-9dfe-dd1d28730c0b" />

Summary 

<img width="411" alt="image" src="https://github.com/user-attachments/assets/0a90c92c-9e3e-41db-b157-89594a8313c7" />

What makes Agents great?
(Memory is the most important)
<img width="858" alt="image" src="https://github.com/user-attachments/assets/b2c124d5-9b4c-46ad-83b9-308f739f8651" />

<img width="863" alt="image" src="https://github.com/user-attachments/assets/5f22e210-1c30-45ea-85ef-cd91117ed818" />
The agents learn from each other

<img width="895" alt="image" src="https://github.com/user-attachments/assets/cc1b3957-a5db-4560-8135-73148025b9b3" />


<img width="337" alt="image" src="https://github.com/user-attachments/assets/3af1a497-f548-43d7-8a2b-c609d388011b" />

<img width="383" alt="image" src="https://github.com/user-attachments/assets/eea65dcf-f4ea-4bd6-a8c2-279734bc9965" />

<img width="356" alt="image" src="https://github.com/user-attachments/assets/e2c53408-6aa4-4319-b6da-7fa9c8799c98" />

<img width="299" alt="image" src="https://github.com/user-attachments/assets/b8595f5a-d094-4403-b4c3-9f190fd00e74" />

<img width="371" alt="image" src="https://github.com/user-attachments/assets/ce29465e-7c7e-46f9-b57b-9de4dba0d1c4" />



<img width="381" alt="image" src="https://github.com/user-attachments/assets/10ded782-bb34-4040-b9cd-d74e59d37143" />

Mental framework for agent creation
<img width="710" alt="image" src="https://github.com/user-attachments/assets/d309f3aa-fb27-4bc1-9270-396a2d169050" />


<img width="449" alt="image" src="https://github.com/user-attachments/assets/9e200907-6c5e-40d9-ad2e-bb0fe4ae628b" />

<img width="880" alt="image" src="https://github.com/user-attachments/assets/ac77f9df-c695-4a9d-b550-ca72e9a81b8e" />

<img width="896" alt="image" src="https://github.com/user-attachments/assets/cbea30df-e7dd-4013-931f-3948c4ff888f" />

<img width="624" alt="image" src="https://github.com/user-attachments/assets/6e9c4c9a-5923-4f5e-bb92-3e9376b166eb" />

<img width="449" alt="image" src="https://github.com/user-attachments/assets/9813422e-f4fb-4fa0-b90c-98763bcf39b2" />
In the ¨indstructions¨ folder, there are markdown files that describes how to treat different sizes companies

<img width="348" alt="image" src="https://github.com/user-attachments/assets/d212485f-5b0b-4d8d-9d27-da11fd1c170f" />


<img width="517" alt="image" src="https://github.com/user-attachments/assets/094e3478-9ad6-4a35-90e4-c0c30e4fba1d" />

<img width="831" alt="image" src="https://github.com/user-attachments/assets/e12be3c6-5c4a-4595-a0cd-bafc0e6a7875" />

```python
# Agent 1: Venue Coordinator
venue_coordinator = Agent(
    role="Venue Coordinator",
    goal="Identify and book an appropriate venue "
    "based on event requirements",
    tools=[search_tool, scrape_tool],
    verbose=True,
    backstory=(
        "With a keen sense of space and "
        "understanding of event logistics, "
        "you excel at finding and securing "
        "the perfect venue that fits the event's theme, "
        "size, and budget constraints."
    )
)
```

```python
 # Agent 2: Logistics Manager
logistics_manager = Agent(
    role='Logistics Manager',
    goal=(
        "Manage all logistics for the event "
        "including catering and equipmen"
    ),
    tools=[search_tool, scrape_tool],
    verbose=True,
    backstory=(
        "Organized and detail-oriented, "
        "you ensure that every logistical aspect of the event "
        "from catering to equipment setup "
        "is flawlessly executed to create a seamless experience."
    )
)
```

```python
# Agent 3: Marketing and Communications Agent
marketing_communications_agent = Agent(
    role="Marketing and Communications Agent",
    goal="Effectively market the event and "
         "communicate with participants",
    tools=[search_tool, scrape_tool],
    verbose=True,
    backstory=(
        "Creative and communicative, "
        "you craft compelling messages and "
        "engage with potential attendees "
        "to maximize event exposure and participation."
    )
)
```

Let the agents fill in the class VenueDetails
```python
from pydantic import BaseModel
# Define a Pydantic model for venue details 
# (demonstrating Output as Pydantic)
class VenueDetails(BaseModel):
    name: str
    address: str
    capacity: int
    booking_status: str
```

```python
venue_task = Task(
    description="Find a venue in {event_city} "
                "that meets criteria for {event_topic}.",
    expected_output="All the details of a specifically chosen"
                    "venue you found to accommodate the event.",
    human_input=True,
    output_json=VenueDetails,
    output_file="venue_details.json",  
      # Outputs the venue details as a JSON file
    agent=venue_coordinator
)
```

This task is waiting for human input
```python
logistics_task = Task(
    description="Coordinate catering and "
                 "equipment for an event "
                 "with {expected_participants} participants "
                 "on {tentative_date}.",
    expected_output="Confirmation of all logistics arrangements "
                    "including catering and equipment setup.",
    human_input=True,
    async_execution=True,
    agent=logistics_manager
)
```

<img width="446" alt="image" src="https://github.com/user-attachments/assets/f0cc0d49-ced9-4173-bdd0-ad984b90f135" />

<img width="644" alt="image" src="https://github.com/user-attachments/assets/2fa2933b-5e58-4a5d-bbb4-af2a800ca01f" />

Adding Process, automatically creates a CrewAI Manager who delegates work among the agents
```python
from crewai import Crew, Process
from langchain_openai import ChatOpenAI

# Define the crew with agents and tasks
financial_trading_crew = Crew(
    agents=[data_analyst_agent, 
            trading_strategy_agent, 
            execution_agent, 
            risk_management_agent],
    
    tasks=[data_analysis_task, 
           strategy_development_task, 
           execution_planning_task, 
           risk_assessment_task],
    
    manager_llm=ChatOpenAI(model="gpt-3.5-turbo", 
                           temperature=0.7),
    process=Process.hierarchical,
    verbose=True
)
```
<img width="440" alt="image" src="https://github.com/user-attachments/assets/d76b9c01-4acb-4ed8-a2b0-333671827024" />

<img width="390" alt="image" src="https://github.com/user-attachments/assets/900e05ed-c84d-4f32-9d85-f7693c908fe5" />

<img width="381" alt="image" src="https://github.com/user-attachments/assets/ef220a7d-6e4c-4a82-8e60-443aa35b53c2" />

Tools
```python
from crewai_tools import (
  FileReadTool,
  ScrapeWebsiteTool,
  MDXSearchTool,
  SerperDevTool
)

search_tool = SerperDevTool()
scrape_tool = ScrapeWebsiteTool()
read_resume = FileReadTool(file_path='./fake_resume.md')
semantic_search_resume = MDXSearchTool(mdx='./fake_resume.md')
```

<img width="825" alt="image" src="https://github.com/user-attachments/assets/a50910a8-2dd1-43dc-8dc2-e1028725afb6" />
