Project Report: FoodRecipe Assistant 🍲
1. Objectives

Build an AI-powered cooking assistant focused exclusively on Indian food recipes.

Integrate OpenAI GPT models for conversational recipe suggestions.

Utilize a dataset of Indian food for structured information (ingredients, time, diet, etc.).

Support two interaction modes: dish name lookup and requirements-based recipe suggestions.

2. Design

Dataset Integration: Loaded CSV dataset with Indian food recipes using Pandas.

System Prompt Engineering: Designed structured system messages for controlled LLM outputs.

Conversation Flow: Implemented two pathways - dish name lookup and structured Q&A.

Validation Layer: Added confirmation to ensure all required keys are collected from the user.

3. Implementation

Implemented in Jupyter Notebook (Python).

Libraries used: pandas, openai, tenacity, IPython.

Notebook loads dataset, initializes conversation, validates inputs, and fetches recipes.

Recipes such as Ghevar and Laddu are used as examples for demonstration.

4. Challenges

Prompt design required careful tuning to ensure model responses remained recipe-focused.

Handling missing information from users required multiple iterations of follow-up questioning.

Dataset limitations: Not all Indian dishes are present, requiring fallback handling.

Ensuring tool outputs (dictionary format) remain consistent across conversations.

5. Lessons Learned

Importance of clear and structured system prompts in LLM applications.

Validation layers significantly improve reliability of conversational agents.

Iterative questioning is essential to collect complete user requirements.

Future improvement scope: Web scraping for missing recipes, deployment as chatbot/web app.
