# FoodRecipe Assistant 🍲  

## 📖 Overview  
This project builds an **AI-powered Cooking Assistant** specialized in **Indian food recipes**.  
The assistant uses **OpenAI GPT models** (Chat Completions API) and a dataset of Indian food to:  
- Suggest recipes based on user preferences (ingredients, diet, time, flavor profile, etc.).  
- Fetch recipes for specific dishes (if available in the dataset).  
- Reject queries unrelated to Indian food.  
- Guide users step by step through conversation until all required details are collected.  

---

## 📂 Project Structure  
- `FoodRecipe_Final.ipynb` → Main notebook with implementation.  
- `Indian_food_with_full_description.csv` → Dataset containing Indian food recipes and details.  

---

## ⚙️ Features  
1. **Dataset Integration**  
   - Reads Indian food dataset (`.csv`) into pandas DataFrame.  
   - Extracts dish names, ingredients, cooking time, region, etc.  

2. **Conversational Assistant**  
   - Uses **system prompts** to guide LLM in recipe suggestions.  
   - Two main interaction modes:  
     - If user provides a **dish name** → Fetch recipe from dataset + internet.  
     - If user provides **requirements** → Ask questions to fill fields (`ingredients, prep_time, cook_time, diet, flavor_profile, course, state, region`).  

3. **Validation Layer**  
   - Confirms that all required fields are present.  
   - If missing, asks clarifying questions.  

4. **Recipe Examples**  
   - Includes detailed recipes for **Laddu** and **Ghevar** as reference.  

---

## 🛠️ Installation  

### 1. Clone this repository  
```bash
git clone <your-repo-url>
cd <your-repo-folder>
```

### 2. Install dependencies  
```bash
pip install -r requirements.txt
```

If `requirements.txt` is not available, install manually:  
```bash
pip install pandas openpyxl openai tenacity
```

---

## ▶️ Usage  

1. **Run the Notebook**  
   Open Jupyter Notebook or JupyterLab and run:  
   ```bash
   jupyter notebook FoodRecipe_Final.ipynb
   ```

2. **Provide Inputs**  
   - Ask for a **specific dish recipe** (e.g., *"Give me recipe for Ghevar"*).  
   - OR provide **preferences** (e.g., *"I want a vegetarian starter from Kerala with prep time 10 mins"*)  

3. **Get Recipe Suggestions**  
   The assistant will:  
   - Parse your request.  
   - Fill missing fields by asking questions.  
   - Suggest a structured recipe dictionary.  

---

## 📊 Example  

**Input:**  
```
I need starter recipe that can take 15 mins prep time and 30 min cook time.  
It should be non-vegetarian and from Kerala.  
```

**Output:**  
```json
{
  "ingredients": "...",
  "diet": "non-vegetarian",
  "prep_time": 15,
  "cook_time": 30,
  "flavor_profile": "savory",
  "course": "starter",
  "state": "Kerala",
  "region": "South",
  "method": "..."
}
```

---

## 🔮 Future Improvements  
- Add **web scraping or API integration** to fetch missing recipes.  
- Enhance **error handling** in user queries.  
- Deploy as a **web or chat application**.  
