# Introduction to AI Orchestration with LangChain and LlamaIndex
This is the repository for the LinkedIn Learning course `Introduction to AI Orchestration with LangChain and LlamaIndex`.
The full course is available from [LinkedIn Learning][lil-course-url].

![lil-thumbnail-url]

Are you ready to dive into the world of AI applications? This course was designed for you. AI orchestration frameworks let you step back from the details of artificial intelligence tools and APIs and instead focus on building more general, effective systems that solve real-world problems. Join instructor M.Joel Dubinko as he explores the business benefits of AI orchestration—faster development, smarter interfaces, lower costs, and more. This course provides an overview of AI fundamentals and key capabilities, like accessing external tools and databases, with a special focus on exploring local models running on your own hardware, alongside or instead of cloud services like those from OpenAI. Every step of the way, Joel offers hands-on demonstrations of two industry-leading frameworks: LangChain and LlamaIndex. By the end of this course, you’ll be prepared to start building chatbots, intelligent agents, and other useful tools, while monitoring for errors and troubleshooting as you go.

Welcome to the course! AI is a fast-changing field, so be sure to check this repo for newer versions of the sample code.

## Installing
1. Clone this repository into your local machine using the terminal (Mac), CMD (Windows), or a GUI tool like SourceTree.
2. Ensure you have Python 3.10 or later (version 3.11 recommended)
3. To prevent conflicts with other installed software on your computer, the author recommends setting up a virtual environment as follows: 
   `python3.11 -m venv .venv`
4. Activate the virtual environment with one of these commands:
   ```
   # Linux or Mac 
   $ source .venv/bin/activate 
   
   # Windows CMD
   C:\> .venv\Scripts\activate.bat
   
   # Windows PowerShell
   PS C:\> .venv\Scripts\Activate.ps1
   ```
5. Install the necessary Python packages: (use the `upgrade` flag to ensure you have current versions)
   ```
   pip install --upgrade openai
   pip install --upgrade langchain
   pip install --upgrade llama-index
   pip install --upgrade langchain-openai
   ```
6. Specific projects in this course might have additional optional requirements. If so, it will be noted within the relevant video.

### Updates

Recent versions of LM Studio have changed the UI from what's shown in the videos. These are generally welcome
improvements. For example the maximum context length and other model parameters are viewable in the sidebar.

Recent versions of LlamaIndex have changed their import and package structure in a way that breaks existing code.
In many cases, you can fix imports as follows:

   ```
   # before
   from llama_index.llms import OpenAILike

   # after
   from llama_index.core.llms import OpenAILike
   ```

Specific third party components require installing new packages. These will be noted in comments. Example:
   ```
   # pip install llama-index-embeddings-huggingface
   from llama_index.embeddings.huggingface import HuggingFaceEmbedding
   ```

For code in Chap04, From March 1, 2024, LlamaHub has been deprecated and most projects migrated into LlamaIndex. (sort of--it's complicated)
Specifically:
   ```
   # before
   # pip install llama_hub
   from llama_hub.tools.bing_search import BingSearchToolSpec

   # after
   # pip install llama-index-tools-bing-search
   from llama_index.tools.bing_search import BingSearchToolSpec
   ```

Additionally, LlamaIndex `ServiceContext` has been deprecated and replaced with `Settings`. See Ch02/rag_llamaindex.py for updated sample code.

LangChain too has changed their import structure, though as of this writing it produces warnings rather than errors. In many cases you will need to import from langchain_community or langchain_openai as follows:
   ```
   #before
   from langchain.chat_models import ChatOpenAI

   # after
   # pip install langchain-openai
   from langchain_openai.chat_models import ChatOpenAI
   ```

### Instructor

M. Joel Dubinko
Software Generalist | Consultant | Instructor | Problem Solver


Check out my other courses on [LinkedIn Learning][URL-instructor-home].



[lil-course-url]: https://www.linkedin.com/learning/introduction-to-ai-orchestration-with-langchain-and-llamaindex
[lil-thumbnail-url]: https://media.licdn.com/dms/image/D560DAQEi6KQmA4fF1Q/learning-public-crop_675_1200/0/1707936616297?e=2147483647&v=beta&t=3vzvDRzpKq9Nd99ss8r2pqMZmyTOKYgKwk825XoSEHU
[URL-instructor-home]: https://www.linkedin.com/learning/instructors/m-joel-dubinko?u=104
