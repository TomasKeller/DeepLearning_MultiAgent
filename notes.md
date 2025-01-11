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

