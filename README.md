# CrewAI Blog Generator

A Jupyter notebook that uses a sequential CrewAI crew to research a topic and turn it into a polished, beginner-friendly blog post in Markdown.

## How it works

The crew has four agents:

1. **Researcher** gathers facts, examples, use cases, and references using web search.
2. **Analyst** turns the research into a structured outline.
3. **Writer** drafts the blog post from the outline.
4. **Editor** improves clarity and flow and returns the final post.

The notebook uses Groq-hosted language models and Serper for web search.

## Requirements

- Python and Jupyter Notebook
- A [Groq API key](https://console.groq.com/keys)
- A [Serper API key](https://serper.dev/)

## Run the notebook

1. Clone this repository and open `crewai_blog_project.ipynb` in Jupyter.
2. Install the notebook dependencies by running its first cell, or run:

   ```bash
   pip install crewai crewai-tools python-dotenv
   ```

3. Create a `.env` file in the project directory with your own keys:

   ```dotenv
   GROQ_API_KEY=your_groq_api_key
   SERPER_API_KEY=your_serper_api_key
   ```

4. Run the notebook cells in order. When prompted, enter the topic for the blog post.
5. The final edited Markdown post is printed at the end of the run.

Keep your real API keys private. The `.env` file is excluded from Git.

## Screenshots

### Crew starts researching

![Crew execution and research task start](screenshots/Screenshot%202026-11-18%20220407.png)

### Web search results

![Serper search results during research](screenshots/Screenshot%202026-11-18%20220417.png)

### Research output

![Research agent final answer](screenshots/Screenshot%202026-11-18%20220430.png)

### Blog outline

![Content analyst blog outline](screenshots/Screenshot%202026-11-18%20220443.png)

### Blog draft

![Blog writer draft](screenshots/Screenshot%202026-11-18%20220452.png)

### Completed blog

![Crew completion and final blog output](screenshots/Screenshot%202026-11-18%20220505.png)
