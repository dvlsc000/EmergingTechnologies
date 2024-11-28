# 📚 Third-Order Letter Approximation & ELIZA Chatbot Project

Welcome to the **Third-Order Letter Approximation & ELIZA Chatbot** project! This repository encompasses tasks ranging from text analysis using trigram models to building a classic ELIZA chatbot interface. Dive in to explore the functionalities and contributions of each component.

---

## 📜 Table of Contents

- [📚 Third-Order Letter Approximation & ELIZA Chatbot Project](#-third-order-letter-approximation--eliza-chatbot-project)
  - [📋 Tasks Overview](#-tasks-overview)
    - [🔍 Task 1: Third-Order Letter Approximation Model](#-task-1-third-order-letter-approximation-model)
    - [✍️ Task 2: Third-Order Letter Approximation Generation](#️-task-2-third-order-letter-approximation-generation)
    - [📈 Task 3: Analyze Your Model](#-task-3-analyze-your-model)
    - [💾 Task 4: Export Model as JSON File](#-task-4-export-model-as-json-file)
  - [🤖 ELIZA Chatbot](#-eliza-chatbot)
    - [🔧 Project Structure](#-project-structure)
    - [✨ Features](#-features)
    - [🚀 Usage](#-usage)
    - [📂 Code Overview](#-code-overview)
  - [📁 File Structure](#-file-structure)
  - [🔗 License](#-license)
  - [🙌 Contributing](#-contributing)
  - [📞 Contact](#-contact)

---

## 📋 Tasks Overview

### 🔍 Task 1: Third-Order Letter Approximation Model

#### **Overview**
Implement a **third-order letter approximation model** that analyzes five plain-text works from Project Gutenberg. This model counts the occurrences of every three-character sequence (trigram) in the cleaned text, providing insights into the frequency of specific letter sequences.

#### **Project Gutenberg Works**
- **Selection Criteria:**
  - Plain Text UTF-8 format.
  - Contains only ASCII characters: letters, spaces, and full stops.
- **File Naming:** `file1`, `file2`, `file3`, `file4`, `file5` for streamlined usage.

#### **Function Descriptions**

1. **`load_and_clean_text(file_paths)`**
   - **Purpose:** Loads multiple text files, removes unwanted characters, and converts all characters to uppercase.
   - **Parameters:**
     - `file_paths` (List[str]): Paths to the Project Gutenberg text files.
   - **Returns:** `str` – A cleaned string ready for trigram analysis.

2. **`generate_trigrams(text)`**
   - **Purpose:** Creates a trigram model by counting every three-character sequence in the cleaned text.
   - **Parameters:**
     - `text` (str): Cleaned text for trigram extraction.
   - **Returns:** `Dict[str, int]` – Dictionary with trigrams as keys and their counts as values.

3. **`display_top_trigrams(trigram_counts, n=100)`**
   - **Purpose:** Displays the top `n` most frequent trigrams.
   - **Parameters:**
     - `trigram_counts` (Dict[str, int]): Trigram frequency dictionary.
     - `n` (int, optional): Number of top trigrams to display. *(Default: 100)*
   - **Displays:** Top `n` trigrams directly in the console.

---

### ✍️ Task 2: Third-Order Letter Approximation Generation

#### **Overview**
Extend the trigram model from Task 1 to generate a 10,000-character-long string. The model predicts the next character based on the frequency of trigrams, following the patterns identified in the cleaned text.

#### **Function Descriptions**

1. **`generate_next_char(trigram_counts, prev_two_chars)`**
   - **Purpose:** Predicts the next character based on the previous two characters using the trigram model.
   - **Parameters:**
     - `trigram_counts` (Dict[str, int]): Trigram frequencies from Task 1.
     - `prev_two_chars` (str): The preceding two characters in the current sequence.
   - **Returns:** `str` – The predicted next character.

2. **`generate_text(trigram_counts, length=10000)`**
   - **Purpose:** Generates a lengthy string by iteratively predicting the next character.
   - **Parameters:**
     - `trigram_counts` (Dict[str, int]): Trigram frequency dictionary.
     - `length` (int, optional): Desired length of the generated text. *(Default: 10,000 characters)*
   - **Returns:** `str` – Generated text of specified length.

---

### 📈 Task 3: Analyze Your Model

#### **Overview**
Assess the quality of the generated text by calculating the percentage of valid English words. This analysis provides insight into the model's ability to produce coherent language sequences.

#### **Function Descriptions**

1. **`load_word_list(file_path)`**
   - **Purpose:** Loads a list of valid English words from a specified file.
   - **Parameters:**
     - `file_path` (str): Path to `words.txt`, containing valid English words.
   - **Returns:** `Set[str]` – Set of uppercase English words.

2. **`calculate_percentage_of_real_words(generated_text, valid_words)`**
   - **Purpose:** Calculates the percentage of valid English words in the generated text.
   - **Parameters:**
     - `generated_text` (str): Text generated by the trigram model.
     - `valid_words` (Set[str]): Set of valid English words.
   - **Returns:** `float` – Percentage of valid English words in the generated text.

---

### 💾 Task 4: Export Model as JSON File

#### **Overview**
Export the trigram model created in Task 1 to a JSON file. This enables future access to the model data or integration with other projects.

#### **Function Description**

- **`export_trigram_model_to_json(trigram_counts, filename='trigram.json')`**
  - **Purpose:** Exports the trigram model to a JSON file.
  - **Parameters:**
    - `trigram_counts` (Dict[str, int]): Trigram model to export.
    - `filename` (str, optional): Name of the JSON file. *(Default: `trigram.json`)*
  - **Result:** Trigram model saved as a JSON file in the specified location.

---

## 🤖 ELIZA Chatbot

### **Overview**
A web-based **ELIZA chatbot** inspired by Joseph Weizenbaum's early natural language processing program from the 1960s. ELIZA simulates conversation by using predefined responses to keywords and patterns in user input. This project features a JavaScript-based chatbot interface that utilizes regular expressions to parse user input and respond conversationally.

### 🔧 Project Structure

1. **`index.html`**
   - Defines the chatbot's HTML structure.
2. **`eliza.js`**
   - Contains ELIZA's response logic, input processing, and chat management functions.
3. **`style.css`**
   - Styles the chatbot's UI, including animations and layout.

### ✨ Features

- **🧠 Natural Language Processing with Regular Expressions**
  - Uses regex patterns to match user input and select appropriate responses.
  
- **👥 User-Friendly Interface**
  - Visually appealing chat history with timestamps and seamless interaction flow.
  
- **🔄 Reset Management**
  - Ability to reset the chat history for a fresh conversation.
  
- **📱 Responsive Design**
  - Adaptive layout for optimal experience across various devices and screen sizes.

### 🚀 Usage

1. **Open the Chat Interface**
   - Type a message in the input box at the bottom of the chat window and press Enter or click the send button to start chatting.
   
2. **Interact with ELIZA**
   - ELIZA analyzes your input, matches it against known patterns, and responds accordingly.
   
3. **Reset Chat**
   - Click the reset button in the header to clear the chat history and begin anew.

### 📂 Code Overview

#### **`eliza.js`**

- **Response Patterns**
  - `elizaResponses` array contains objects with `pattern` and `response` properties.
  
- **`getElizaResponse()` Function**
  - Iterates through `elizaResponses` to find a pattern match for the user input and returns a formatted response.
  
- **`processInput()` Function**
  - Manages user input, clears the input field, and displays ELIZA's response.
  
- **`addMessage()` Function**
  - Adds messages to the chat window with timestamps and scrolls to the latest message.
  
- **`resetChat()` Function**
  - Clears the chat history for a new conversation.

#### **`style.css`**

- **Chat Container**
  - Center-aligned with a gradient background and glass effect.
  
- **Messages Styling**
  - Distinct styles for user and bot messages, featuring speech bubble shapes, animations, and timestamps.
  
- **Input Area**
  - Rounded input field with a custom send button for enhanced aesthetics.

#### **`index.html`**

- **Header**
  - Displays the chatbot title and reset button.
  
- **Chat Box**
  - Contains chat messages with `user` and `bot` classes for styling.
  
- **Input Field**
  - Text input for user messages and a send button to trigger responses.

---

## 📁 File Structure

