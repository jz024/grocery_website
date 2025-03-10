---
title: Methods
layout: page
---

<div style="text-align: center;">
    <img src="assets/useflow.png" alt="Use flow of SmartCart" style="width:100%;">
    <p><strong>Use flow of SmartCart</strong><br>
    (1) We collect user data including dietary restrictions, culinary preferences, and location;<br>
    (2) User chats with our agent to determine what dish they want to cook;<br>
    (3) Agent generates a shopping list and (4) store recommendations;<br>
    finally, (5) the user either navigates to the stores or uses our tailored checkout experience.</p>
</div>

## Introduction

The process of meal planning, which involves selecting recipes, preparing shopping lists, and sourcing ingredients, can be time-consuming and inefficient for busy home cooks. As modern lifestyles become more fast-paced, individuals increasingly seek solutions that reduce the effort and complexity of daily meal preparation.

Despite the abundance of recipes available online, many existing meal-planning solutions lack personalization or efficient grocery store integration, leaving users to manually handle key tasks like ingredient sourcing and store selection. To address these challenges, we propose a specialized language model (LLM) agent designed to streamline the meal-planning process.

Our system leverages state-of-the-art technologies in natural language processing, backend development, and location-based services to create a seamless, user-friendly experience. The solution integrates:
- Dynamic user interaction for personalized meal recommendations
- Automated shopping list generation
- Intelligent store recommendations using Google Maps API
- Comprehensive recipe guidance

## Methods

Our system architecture consists of three main components:

### Frontend (React Native)
- Cross-platform mobile application supporting Android and iOS
- User-friendly interface for inputting meal preferences and dietary restrictions
- Interactive suggestion pages for meal selection
- Detailed results display including store locations and cooking instructions
- RESTful API integration for backend communication

### Middle Layer (Google APIs)
- Google Maps API for nearby grocery store information
- Google Places API for ingredient availability search
- Google Distance Matrix API for store prioritization
- Dynamic location-based data processing

### Backend Infrastructure
1. **RAG Model**
   - Personalized response generation
   - Recipe retrieval and recommendation
   - Shopping list compilation
   - Cooking instruction generation

2. **MongoDB Database**
   - Recipe storage
   - User profile management
   - Meal plan tracking
   - Store-specific product details

The workflow integrates these components to provide:
- Real-time data processing
- Location-based optimization
- Personalized meal recommendations
- Comprehensive shopping guidance

The proposed system integrates a React Native mobile application as the frontend, Google
APIs as the middle layer, and a backend consisting of Firebase Firestore and MongoDB to
create a streamlined meal-planning experience. The architecture ensures seamless interac-
tion between components, enabling dynamic user input, location-based store recommen-
dations, and personalized recipe generation.
The frontend is developed using React Native, enabling cross-platform functionality for both
Android and iOS devices. The mobile app serves as the primary interface for users, allowing
them to input meal preferences, dietary restrictions, and desired food profiles. Users can
view meal suggestions, comprehensive shopping lists, and nearby store recommendations.
The interface is designed with user-friendly features, including interactive suggestion pages
and detailed results pages that present store locations, product availability, and step-by-
step cooking instructions. The React Native app communicates with the backend through
RESTful API calls to ensure efficient data transfer.

The backend is built using FastAPI, integrating Firebase Firestore as the main data store
for user preferences and MongoDB for storing chat history and shopping lists. Firebase
Firestore allows for real-time updates and ensures that user preferences are dynamically.
When a user provides meal preferences,
the backend retrieves this information from Firebase Firestore and cross-references it with
stored chat history to improve response accuracy. MongoDB stores past interactions, en-
abling the LLM agent to retrieve relevant data when generating responses. The system also
integrates Google Maps API to identify grocery stores based on proximity, price, and prod-
uct availability. The Stripe API is incorporated to facilitate seamless checkout and payment
processing if users wish to purchase items online.

The workflow begins when a user inputs their meal preferences through the mobile appli-
cation. These preferences are sent to the backend, where they are stored and processed
in Firebase Firestore. The system retrieves recipe recommendations based on the user’s di-
etary preferences and generates a shopping list of necessary ingredients. Next, the Google
Maps API is used to identify nearby grocery stores that stock the required items. The sys-
tem prioritizes stores based on factors such as distance, price, and availability. If an item
is unavailable at the primary store, the system searches for alternative stores to ensure all
ingredients can be sourced. The backend then compiles a structured response, which is
sent back to the frontend, providing the user with an optimized shopping plan, grocery
store recommendations, and step-by-step cooking instructions.
