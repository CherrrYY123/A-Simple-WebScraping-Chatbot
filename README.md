# A-Simple-WebScraping-Chatbot
The "Web Scraping Chatbot" project develops an interactive system that parses online recipes and offers a conversational interface for users. It extracts recipe information from a given URL and enables users to navigate through the recipe steps in a chatbot-like manner.

## Features
- **Recipe Parsing**: Retrieves and processes recipe data from a specified URL.
- **Conversational Interface**: Engages users, guiding them through recipe steps and answering questions.
- **Step Navigation**: Allows users to navigate between steps, view the current step, or get information about the recipe.

## Data Extraction
The chatbot begins by fetching the HTML content of the provided recipe URL using `urllib.request.urlopen()`. It then parses the HTML with BeautifulSoup to extract the recipe title, description, and ingredients list.

## Text Processing
The extracted text is cleaned and filtered to remove unnecessary characters and format the content for easier manipulation. This includes removing newlines, extra spaces, and filtering out irrelevant content.

## Recipe Navigation
The `RecipeNavigator` class handles navigation through recipe steps, allowing users to:
  - Move between steps
  - View the current step
  - Jump to specific steps

## Conversational Interface
The conversational interface uses **TF-IDF vectorization** and **cosine similarity** to match user queries with recipe steps. **Fuzzy matching** is also used to enhance query understanding.

## Using the Chatbot
### Sample Links:
- [Chicken Ricotta Meatballs](https://www.allrecipes.com/chicken-ricotta-meatballs-recipe-8683251)
- [Risotto alla Pavese](https://www.allrecipes.com/recipe/274484/risotto-alla-pavese/)
- [Classic and Simple Meat Lasagna](https://www.allrecipes.com/recipe/218091/classic-and-simple-meat-lasagna/)
- [Vindaloo](https://en.wikipedia.org/wiki/Vindaloo)

### Sample Questions:
- *How can I get cutlery for this?*
- *How to boil water?*
- *How to use an oven?*
- *Give cooking steps.*
- *Take me to the current step.*
- *What are the recipe ingredients?*
- *What is the oven temperature for this?*
- *Where in India can I find this?*
- *Is it from Goa?*
- *Find chicken Vindaloo in Mumbai.*

## Technologies Used
- **Python Libraries**: `nltk`, `numpy`, `beautifulsoup4`, `requests`, `textblob`, `fuzzywuzzy`, `scikit-learn`
- **Web Scraping**: BeautifulSoup for extracting data from HTML.
- **Natural Language Processing**: NLTK for tokenization and text processing.
- **Text Similarity**: TF-IDF and cosine similarity for matching user queries with recipe content.

## Installation
To set up the project, install the required Python libraries using the `requirements.txt` file:

```bash
pip install -r requirements.txt

