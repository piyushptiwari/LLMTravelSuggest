TravelAssistAI Chatbot Using LLM

A chatbot designed to assist users with travel queries and recommend holiday packages using a dataset and OpenAI APIs.

Introduction In today’s fast-paced world, planning a holiday can be overwhelming due to too many choices and lack of personalized help. TravelAssist AI addresses this by utilizing large language models (LLMs) and rule-based systems to recommend tailored holiday packages based on user input.

Problem Statement Using a dataset (holiday packages from Kaggle), the chatbot provides recommendations based on user preferences like destination, duration, and budget. The original dataset had 30k rows but was reduced to 4 due to OpenAI timeout issues.

Approach

Conversation & Information Gathering: The chatbot uses LLMs to understand user needs and asks relevant questions.
Information Extraction: Rule-based functions extract matching holiday packages.
Personalized Recommendations: The chatbot engages in further dialogue to refine recommendations.
System Design The chatbot consists of several layers:

Intent Clarity
Intent Confirmation
Product Mapping
Information Extraction
Product Recommendation
Functions

initialize_conversation(): Starts a conversation.
get_chat_model_completions(): Generates chatbot responses.
moderation_check(): Filters inappropriate content.
intent_confirmation_layer(): Confirms user intent (destination, package, origin, duration, budget).
dictionary_present(): Ensures user data is stored in a Python dictionary.
compare_holiday_with_user(): Matches user preferences to holiday packages.
Challenges & Limitations

Limited origin cities (New Delhi and Mumbai).
Only four holiday options available due to dataset trimming.
Timeout issues with OpenAI API when using larger datasets.
The bot does not recommend alternative options when user input doesn't match available data.
Despite these limitations, TravelAssist AI helps users find relevant holiday packages, personalizing travel recommendations and providing seamless interaction via a Flask-based UI.
