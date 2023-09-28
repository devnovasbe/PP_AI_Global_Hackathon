# PP_AI_Global_Hackathon

Zero waste app leverages AI to help avoid wating food and managing the food inventory in an efficient way.

It integrates AI builder object recognition to scan a fridge or a shelf, and tell exactly what is missing from the pre-defined shopping list.

So, there are 4 parts:

 - 'Camera', where user can leverage AI builder to scan his fridge and calculate the shopping list
 - 'My List' where the user defines what he needs to buy
 - 'Shopping list' where the user will find the calculated shopping list, based on the scan made by AI builder
 - 'Recipes' where user can leverage chat GPT to get recipies with the already existent items, and then save the ones that he finds useful
 - 'Settings' where the user can define his profile and inform the app about some food restrictions, etc.


Main components:

 - Custom connectors to communicate with our webservice and Walmart API
 - Power Automate flow to leverage the developed webservice and Walmart API through custom connectors
 - Canvas app
 - AI model already trained
