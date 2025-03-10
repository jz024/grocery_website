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
## Results

The evaluation of our meal-planning assistant, based on user feedback from the SmartCart
survey, highlights its effectiveness in simplifying meal selection and enhancing the grocery
shopping experience. A majority of users (82%) found that the system made meal plan-
ning easier, with many appreciating the structured approach to generating personalized
meal recommendations. However, some users noted that certain meal suggestions did not
fully align with their preferences or contained hard-to-find ingredients. In terms of grocery
shopping efficiency, 75% of users reported a positive impact, particularly due to the auto-
matically generated shopping lists and store recommendations. Nonetheless, some users
encountered occasional mismatches between the recommended stores and actual product
availability due to a lack of real-time inventory tracking. Route optimization was also well-
received, with 79% of users finding it helpful for planning their shopping trips, though those
in rural areas reported difficulties due to limited grocery store data. Personalization was a
strong aspect of the system, as 88% of users found the meal recommendations relevant to
their tastes, and 90% confirmed that their dietary restrictions were accurately considered.
However, some users expressed a desire for more transparency in how recommendations
were generated, along with additional flexibility in ingredient substitutions. These findings
suggest that while the assistant effectively streamlines meal planning and grocery shopping
for most users, improvements in real-time pricing and inventory tracking, expanded gro-
cery store coverage, and enhanced customization options could further optimize the user
experience.

## Discussion

The evaluation results demonstrate that our meal-planning assistant effectively streamlines
meal selection and grocery shopping for most users. The integration of Firebase Firestore,
FastAPI, and Google Maps API enabled a seamless experience, with meal recommendations
and shopping lists tailored to user preferences. Compared to existing meal-planning appli-
cations such as Mealime and Paprika, our system offers a higher degree of personalization
and convenience by incorporating real-time store location data. While AI-driven recommen-
dation systems, such as IBM Watson Meal Planner, provide personalized meal suggestions,
they lack the direct integration with grocery stores and automated shopping list generation
that our system provides.
Despite these advantages, some challenges remain. Users in less densely populated areas
experienced difficulty finding relevant grocery store recommendations due to limited store
data, a limitation also observed in prior studies on location-based retail applications. While
the system aimed to optimize cost efficiency, the absence of real-time store pricing some-
times led to inaccurate cost estimates, a common issue in online grocery shopping platforms
that rely on static pricing models. Additionally, some users expressed interest in more flex-
ible meal customization options, such as ingredient substitutions and dietary-specific meal
plans, indicating a need for greater adaptability in future iterations.
To further improve the system, several enhancements can be considered. Implementing
real-time pricing APIs from grocery retailers could improve cost estimation accuracy, ad-
dressing a key limitation of the current approach. Expanding the ingredient substitution
feature would provide users with greater flexibility in adjusting their meal plans based on
availability and dietary preferences. Additionally, increasing store data coverage in rural
areas through partnerships with regional grocery chains could enhance the system’s usabil-
ity in underserved locations. Another promising direction is improving the transparency
of recommendation logic, allowing users to understand why certain meal suggestions are
made, which could improve trust and user engagement.
Overall, the SmartCart system demonstrates strong potential as a practical solution for meal
planning and grocery shopping. While it effectively personalizes meal recommendations
and optimizes grocery store selection, addressing the identified limitations in future iter-
ations will enhance its reliability and user satisfaction. Future work should also explore
machine learning-driven optimization techniques for balancing price, distance, and ingre-
dient availability in real time, further refining the system’s ability to meet user needs. 

## Conclusion

This project presents an innovative meal-planning LLM agent that significantly enhances the
user experience by streamlining meal selection, shopping list generation, and grocery store
recommendations. Through the integration of a React Native frontend, FastAPI backend
services, Firebase Firestore, and Google Maps API, the system provides a seamless, efficient,
and personalized meal-planning assistant for busy home cooks.
The evaluation results demonstrate that the system successfully simplifies meal planning
and grocery shopping, with a majority of users reporting improved efficiency in selecting
meals, generating shopping lists, and planning store visits. The ability to provide person-
alized meal recommendations and optimize grocery store selection was particularly well-
received. However, some limitations were identified, including occasional mismatches in
product availability, challenges in rural areas due to limited store data, and a lack of real-
time pricing information. Additionally, while the majority of users found meal suggestions
relevant, some desired greater flexibility in ingredient substitutions and increased trans-
parency in recommendation logic.
To further enhance the system, future work should focus on integrating real-time pricing
APIs from grocery retailers to provide more accurate cost estimates and product availability
updates. Expanding the ingredient substitution feature would allow users to customize their
shopping lists more effectively based on personal preferences or dietary restrictions. Fur-
thermore, improving store data coverage, particularly in rural and less densely populated
areas, would ensure that users across different regions receive high-quality recommenda-
tions. Additional refinements, such as the ability to prioritize organic or locally sourced in-
gredients and incorporating real-time stock tracking, could further improve the assistant’s
functionality and user satisfaction.
Overall, the results validate the system’s potential as a practical and intelligent solution for
meal planning and grocery shopping. By addressing the identified limitations and incorpo-
rating user-driven improvements, future iterations of the assistant could provide an even
more seamless and adaptable experience, catering to a broader range of users and shopping
needs.