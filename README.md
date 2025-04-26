# Chatbot
A list of chatbot programs to run like rule based and NLP based
## Rulebase_Chatbot
- A Rule-Based Chatbot works by following predefined rules to respond to user queries. It matches keywords in the user's input with specific intents, and then provides a corresponding response based on the matched intent.

#### How It Works
1. Query Matching: The chatbot searches for keywords in the user's query.

2. Intent Mapping: Keywords are mapped to intents (e.g., "hello" → greetings).

3. Response Generation: The chatbot selects a response from the matched intent.

##### Example:
- User: "Hello"
- Bot: "Hi, how can I assist you today?"


#### Limitations
- Limited Flexibility: It only works for exact matches and can't handle varied phrasing without predefined rules.

- Scalability: It’s difficult to manage as the number of keywords and responses increases.

#### Improvements
- Phrase Matching: Match phrases, not just individual words, for better user interaction.

- Best Intent: Choose the most relevant intent when multiple matches occur.

- Fallback: Provide a default response when no intent is matched.

#### Structure
1. Keywords & Intent Mapping: Define keywords (e.g., "hello") and their corresponding intents (e.g., greetings).

2. Intent & Response Mapping: Each intent has multiple possible responses.
#### Output


## NLP Based Chatbot
### 🤖 NLP Chatbot :
This is a simple **NLP-style chatbot** that acts as an import/export assistant. It uses a corpus file (`import_export_knowledge.txt`) and natural language processing techniques to understand and respond to user queries intelligently.

---

#### 🔍 Rule-based vs. NLP-style Chatbot

| Rule-Based Chatbot | NLP-Style Chatbot |
|--------------------|------------------|
| Works on predefined rules | Learns from patterns in data |
| Matches keywords to fixed responses | Understands query context |
| No learning involved | Uses NLP for dynamic responses |
| Random or template-based answers | Responses based on vector similarity |

---

#### 🧠 How It Works

1. **Data Collection**: Uses a static corpus file (e.g., `import_export_knowledge.txt`). You can also extend it to use internet-based or user-generated data.
2. **Data Preprocessing**:
   - ✅ **Letter Conversion**
   - ✅ **Tokenization**
   - ✅ **Noise Removal**
   - ✅ **Stop Words Removal**
   - ✅ **Lemmatization**

3. **Encoding with TF-IDF**: Converts user queries into numerical vectors using **TF-IDF** (Term Frequency-Inverse Document Frequency).
4. **Similarity Matching**: Uses **Cosine Similarity** to compare user queries to the corpus and retrieve the most relevant response.

---

#### 📄 Corpus File
Make sure this file is in the **same directory** as your Python chatbot script.

## RNN Chatbot
## 🤖 Why Use RNN Instead of CNN for Chatbots?

Chatbots need to understand **language**, which is **sequential**—words depend on each other for meaning. For example:

> “Tom is a good boy. **He** gets good marks.”
Here, “he” refers to “Tom.” To understand that, we need memory of the earlier words.

### ❌ Why CNN Doesn’t Work Well
- CNNs treat each input **independently**.
- They’re great for images, not for text.
- They **can’t remember** previous words or context.

### ✅ Why RNN Works Better
- RNNs are designed for **sequential data**.
- They **remember previous inputs** and use them to understand current ones.
- Perfect for chatbots where context matters.

---

## 🧠 How AI Chatbot Works (Simple Summary)

- We will give some data, make inferences, and form relationships or functions.
- Getting the **inference from data** is the job of our neural network.
- The chatbot uses a trained RNN to **understand input sentences** and generate **meaningful replies**.

---

## 🛠️ How We Use Machine Learning

We train a **neural network** to learn patterns in conversations:

1. Feed in training data (examples of conversations).
2. Network starts with **random weights**.
3. It predicts a response and compares it to the correct one.
4. Using **gradient descent**, it adjusts the weights to improve.
5. Over time, it learns to give better, more accurate responses.

---

## 🔁 Summary: CNN vs RNN

| Feature     | CNN (Bad for Chatbots) | RNN (Good for Chatbots) |
|-------------|------------------------|--------------------------|
| Memory      | ❌ No                  | ✅ Yes                   |
| Input Type  | Independent            | Sequential               |
| Context     | ❌ Can't keep          | ✅ Can remember          |
