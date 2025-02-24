---
title: Methods
layout: page
---

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

## Results

[Results section will be updated with system performance metrics and user feedback]

## Discussion

[Discussion section will be updated with analysis of system effectiveness and comparison with existing solutions]

## Conclusion

[Conclusion section will be updated with final findings and future improvements]