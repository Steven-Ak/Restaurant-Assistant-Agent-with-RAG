# Restaurant-Assistant-Agent-with-RAG

An **AI-powered conversational agent** designed for restaurants that handles **customer questions, order management, and general inquiries** through Telegram. The system combines **Retrieval-Augmented Generation (RAG)** with **tool-based actions** (Google Sheets) and **agent memory** to deliver accurate, context-aware, and actionable responses.

This project goes beyond a simple chatbot — it is a **multi-intent customer service agent** capable of reasoning, retrieving knowledge, and performing real operations such as creating and canceling orders.

---

![Workflow Image](https://github.com/Steven-Ak/Restaurant-Assistant-Agent-with-RAG/blob/main/Restaurant%20Assistant%20Agent%20with%20RAG%20Workflow%20Screen.png)

---

## ✨ Key Features

* 🤖 **AI Agent Architecture**

  * Central agent responsible for reasoning and tool selection
  * Memory-enabled conversations for better context handling

* 🧠 **Retrieval-Augmented Generation (RAG)**

  * Restaurant knowledge base powered by embeddings
  * Accurate answers to menu, policy, and restaurant-related questions

* 🔀 **Intent Routing (Employee Switch)**

  * Automatically classifies incoming messages into:

    * Questions
    * Orders
    * General conversations

* 🧾 **Order Management via Tools**

  * Create new orders (append to Google Sheets)
  * Read existing orders
  * Cancel/update orders

* 📩 **Telegram Integration**

  * Real-time customer interaction via Telegram Bot API

---

## 🏗️ System Architecture

High-level workflow:

1. **Telegram Trigger**

   * Receives incoming customer messages

2. **Basic LLM Chain**

   * Pre-processes and structures user input

3. **Employee Switch (Rules-based Router)**

   * Classifies intent: Questions / Orders / General

4. **Prompt Modules**

   * Dedicated prompts for each intent type

5. **AI Agent**

   * Uses:

     * LLM reasoning
     * Memory
     * RAG knowledge base
     * External tools (Google Sheets)

6. **Response Delivery**

   * Sends final response back to the customer on Telegram

---

## 📚 Knowledge Base (RAG)

* Restaurant documents (menu, policies, FAQs, etc.) are embedded using **Google Gemini Embeddings**
* Stored in a vector database
* Queried dynamically by the agent when answering customer questions

This ensures:

* Reduced hallucinations
* Up-to-date and domain-specific answers

---

## 🛠️ Tools Used

* **LLM Provider**: OpenRouter (Chat Models)
* **Embeddings**: Google Gemini Embeddings
* **Vector Store**: Supabase Vector Store
* **Order Storage**: Google Sheets
* **Messaging Platform**: Telegram Bot
* **Memory**: Simple conversation memory

---

## 📂 Project Components

* `Telegram Trigger` – Handles incoming Telegram messages
* `Basic LLM Chain` – Message preprocessing
* `Employee Switch` – Intent classification
* `Questions / Orders / General Prompts` – Intent-specific prompting
* `AI Agent` – Core reasoning and orchestration unit
* `orders_sheet_* tools` – Google Sheets operations
* `restaurant_knowledge_base` –  Restaurant Knowledge Base in vector store

---

## 🚀 Use Cases

* Answer customer questions about menu items and prices
* Provide restaurant information (hours, location, policies)
* Take new orders directly from chat
* View or cancel existing orders
* Handle casual or general conversations

---

## 🔮 Future Improvements

* Payment integration
* Admin dashboard for order monitoring
* Analytics on customer interactions

---

⭐ If you find this project interesting, feel free to star the repository!
