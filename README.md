# Smart Product Search Application

## Overview
This repository contains a smart product search application built using Python, SQLite, and Streamlit. The application allows users to search for products, compare prices across different e-commerce platforms, check shipping and refund policies, and apply promo codes. The application uses fuzzy matching for product search and integrates with an LLM (Ollama) for generating summaries and recommendations.

---

## Repository Structure
```
smart-product-search/
├── app.py                  # Main Streamlit application
├── create_db.py            # Script to create and populate the SQLite database
├── data_constants.py       # Contains product data, shipping policies, refund policies, and promo codes
├── products.db             # SQLite database file (generated by create_db.py)
└── README.md               # Documentation
```

---

## Features
1. **Product Search**: Fuzzy matching-based search for products.
2. **Price Comparison**: Compare prices of the same product across multiple platforms.
3. **Shipping Information**: Get estimated delivery dates and shipping costs based on location.
4. **Refund Policies**: View detailed refund and return policies.
5. **Promo Codes**: Apply promo codes to get discounts on products.
6. **AI Summaries**: Generate concise summaries of product details, shipping, and refund policies using an LLM.
7. **Stock Availability**: Check if a product is in stock (simulated).

---

## Design Decisions

### Agent Architecture
The application follows a **modular architecture** with the following components:
1. **Database Layer**: SQLite database (`products.db`) stores product details, shipping policies, refund policies, and promo codes.
2. **Business Logic Layer**: Handles product search, price comparison, shipping and refund policy retrieval, and promo code application.
3. **Presentation Layer**: Streamlit-based UI for user interaction.
4. **AI Integration**: Ollama (LLM) for generating summaries and recommendations.

### Tool Selection
- **SQLite**: Lightweight and easy-to-use database for storing structured data.
- **Streamlit**: Simplifies building interactive web applications with Python.
- **Ollama**: Used for generating AI-powered summaries and recommendations.
- **FuzzyWuzzy**: Provides fuzzy string matching for improved product search.
- **Random**: Simulates stock availability checks (can be replaced with real inventory APIs).

---

## Challenges & Improvements

### Challenges
1. **Fuzzy Matching Limitations**: Fuzzy matching works well for similar strings but may struggle with completely different product names or descriptions.
2. **Stock Simulation**: The current stock availability check is simulated using random values. Integrating with real inventory APIs would improve accuracy.
3. **LLM Latency**: Generating AI summaries can be slow, depending on the LLM's response time.
4. **Location-Based Shipping**: Shipping estimates are based on predefined location factors. Real-time shipping APIs could provide more accurate estimates.

### Improvements
1. **Real Inventory Integration**: Replace the simulated stock check with real-time inventory APIs.
2. **Enhanced Fuzzy Matching**: Use advanced NLP techniques (e.g., embeddings) for better product search.
3. **Caching**: Cache LLM responses to reduce latency for frequently searched products.
4. **Real-Time Shipping APIs**: Integrate with shipping carriers (e.g., FedEx, DHL) for accurate delivery estimates.
5. **User Authentication**: Add user accounts to save search history and preferences.
6. **Multi-Language Support**: Extend the application to support multiple languages.

---

## Comparative Conceptual Map
*(To be added)*

---

## Short Written Analysis
*(To be added)*

---

## Open Questions & References
*(To be added)*

---

## How to Run the Application
1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/smart-product-search.git
   cd smart-product-search
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Create and populate the database:
   ```bash
   python create_db.py
   ```
4. Run the Streamlit application:
   ```bash
   streamlit run app.py
   ```
5. Open the application in your browser and start searching for products!

---

## Video Recording
*(To be added)*

---

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
