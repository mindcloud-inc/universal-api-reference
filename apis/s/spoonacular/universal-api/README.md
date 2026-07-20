# <img src="https://images.mindcloud.co/apps/icons/spoonacular-icon-final_1776185030235.png" alt="Spoonacular logo" width="28" height="28"> Spoonacular: Universal API

Spoonacular provides recipe, ingredient, product, menu item, meal planning, wine, image analysis, and food utility APIs for food and cooking applications.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/spoonacular/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 104
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://spoonacular.com/food-api
- **Vendor API docs:** https://spoonacular.com/food-api/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Analyze a Recipe Search Query](actions/analyze-a-recipe-search-query.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/spoonacular/latest/actions/analyze-a-recipe-search-query?connectionId=$CONNECTION_ID&q=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (104)

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Add Custom Foods](actions/add-custom-foods.md) | POST | Creates a custom food in Spoonacular. |
| [Add Meal Plan Template](actions/add-meal-plan-template.md) | POST | Creates a meal plan template in Spoonacular. |
| [Add to Meal Plan](actions/add-to-meal-plan.md) | POST | Adds an item to a Spoonacular meal plan. |
| [Add to Shopping List](actions/add-to-shopping-list.md) | POST | Adds an item to a Spoonacular shopping list. |
| [Analyze a Recipe Search Query](actions/analyze-a-recipe-search-query.md) | GET | Analyzes a recipe search query in Spoonacular. |
| [Analyze Recipe](actions/analyze-recipe.md) | GET | Analyzes recipe data in Spoonacular. |
| [Analyze Recipe Instructions](actions/analyze-recipe-instructions.md) | GET | Analyzes recipe instructions in Spoonacular. |
| [Autocomplete Ingredient Search](actions/autocomplete-ingredient-search.md) | GET | Autocompletes ingredient names in Spoonacular. |
| [Autocomplete Menu Item Search](actions/autocomplete-menu-item-search.md) | GET | Autocompletes menu items in Spoonacular. |
| [Autocomplete Product Search](actions/autocomplete-product-search.md) | GET | Autocompletes grocery products in Spoonacular. |
| [Autocomplete Recipe Search](actions/autocomplete-recipe-search.md) | GET | Autocompletes recipe names in Spoonacular. |
| [Classify Cuisine](actions/classify-cuisine.md) | GET | Classifies a recipe cuisine with Spoonacular. |
| [Classify Grocery Product](actions/classify-grocery-product.md) | GET | Classifies a grocery product with Spoonacular. |
| [Classify Grocery Product Bulk](actions/classify-grocery-product-bulk.md) | GET | Classifies grocery products in bulk with Spoonacular. |
| [Clear Meal Plan Day](actions/clear-meal-plan-day.md) | DELETE | Clears a day from a Spoonacular meal plan. |
| [Compute Glycemic Load](actions/compute-glycemic-load.md) | GET | Computes ingredient glycemic load with Spoonacular. |
| [Compute Ingredient Amount](actions/compute-ingredient-amount.md) | GET | Computes an amount for a Spoonacular ingredient. |
| [Compute Shopping List](actions/compute-shopping-list.md) | GET | Computes a shopping list with Spoonacular. |
| [Connect User](actions/connect-user.md) | POST | Connects a user to Spoonacular meal planning. |
| [Conversation Suggests](actions/conversation-suggests.md) | GET | Retrieves chatbot suggestions from Spoonacular. |
| [Convert Amounts](actions/convert-amounts.md) | GET | Converts ingredient amounts in Spoonacular. |
| [Create Recipe Card](actions/create-recipe-card.md) | POST | Creates a recipe card in Spoonacular. |
| [Delete from Meal Plan](actions/delete-from-meal-plan.md) | DELETE | Deletes an item from a Spoonacular meal plan. |
| [Delete from Shopping List](actions/delete-from-shopping-list.md) | DELETE | Deletes an item from a Spoonacular shopping list. |
| [Delete Meal Plan Template](actions/delete-meal-plan-template.md) | DELETE | Deletes a meal plan template from Spoonacular. |
| [Detect Food in Text](actions/detect-food-in-text.md) | GET | Detects food entities in text with Spoonacular. |
| [Dish Pairing for Wine](actions/dish-pairing-for-wine.md) | GET | Retrieves wine dish pairings from Spoonacular. |
| [Equipment by ID](actions/equipment-by-id.md) | GET | Retrieves equipment data for a Spoonacular recipe. |
| [Equipment by ID Image](actions/equipment-by-id-image.md) | GET | Retrieves a recipe equipment image from Spoonacular. |
| [Equipment by ID Widget](actions/equipment-by-id-widget.md) | GET | Retrieves a recipe equipment widget from Spoonacular. |
| [Equipment Widget](actions/equipment-widget.md) | GET | Generates a recipe equipment widget in Spoonacular. |
| [Estimate Nutrients from Image](actions/estimate-nutrients-from-image.md) | GET | Estimates nutrients from an image in Spoonacular. |
| [Estimate Nutrition by Dish Name](actions/estimate-nutrition-by-dish-name.md) | GET | Estimates nutrition for a dish name in Spoonacular. |
| [Extract Recipe from Website](actions/extract-recipe-from-website.md) | GET | Extracts recipe data from a website with Spoonacular. |
| [Generate Meal Plan](actions/generate-meal-plan.md) | GET | Generates a meal plan with Spoonacular. |
| [Generate Shopping List](actions/generate-shopping-list.md) | GET | Generates a shopping list in Spoonacular. |
| [Get Analyzed Recipe Instructions](actions/get-analyzed-recipe-instructions.md) | GET | Retrieves analyzed instructions for a Spoonacular recipe. |
| [Get Comparable Products](actions/get-comparable-products.md) | GET | Retrieves comparable grocery products from Spoonacular. |
| [Get Ingredient Information](actions/get-ingredient-information.md) | GET | Retrieves ingredient details from Spoonacular. |
| [Get Ingredient Substitutes](actions/get-ingredient-substitutes.md) | GET | Retrieves ingredient substitutes from Spoonacular. |
| [Get Ingredient Substitutes by ID](actions/get-ingredient-substitutes-by-id.md) | GET | Retrieves substitutes for a Spoonacular ingredient. |
| [Get Meal Plan Day](actions/get-meal-plan-day.md) | GET | Retrieves a daily meal plan from Spoonacular. |
| [Get Meal Plan Template](actions/get-meal-plan-template.md) | GET | Retrieves a meal plan template from Spoonacular. |
| [Get Meal Plan Templates](actions/get-meal-plan-templates.md) | GET | Retrieves meal plan templates from Spoonacular. |
| [Get Meal Plan Week](actions/get-meal-plan-week.md) | GET | Retrieves a weekly meal plan from Spoonacular. |
| [Get Menu Item Information](actions/get-menu-item-information.md) | GET | Retrieves menu item details from Spoonacular. |
| [Get Product Information](actions/get-product-information.md) | GET | Retrieves grocery product details from Spoonacular. |
| [Get Random Recipes](actions/get-random-recipes.md) | GET | Retrieves random recipes from Spoonacular. |
| [Get Recipe Information](actions/get-recipe-information.md) | GET | Retrieves recipe details from Spoonacular. |
| [Get Recipe Information Bulk](actions/get-recipe-information-bulk.md) | GET | Retrieves details for multiple Spoonacular recipes. |
| [Get Shopping List](actions/get-shopping-list.md) | GET | Retrieves a shopping list from Spoonacular. |
| [Get Similar Recipes](actions/get-similar-recipes.md) | GET | Retrieves recipes similar to a Spoonacular recipe. |
| [Image Analysis by File](actions/image-analysis-by-file.md) | GET | Analyzes a food image with Spoonacular. |
| [Image Analysis by URL](actions/image-analysis-by-url.md) | GET | Analyzes a food image URL with Spoonacular. |
| [Image Classification by File](actions/image-classification-by-file.md) | GET | Classifies a food image with Spoonacular. |
| [Image Classification by URL](actions/image-classification-by-url.md) | GET | Classifies a food image URL with Spoonacular. |
| [Ingredient Search](actions/ingredient-search.md) | GET | Searches for ingredients in Spoonacular. |
| [Ingredients by ID](actions/ingredients-by-id.md) | GET | Retrieves ingredient data for a Spoonacular recipe. |
| [Ingredients by ID Image](actions/ingredients-by-id-image.md) | GET | Retrieves a recipe ingredients image from Spoonacular. |
| [Ingredients by ID Widget](actions/ingredients-by-id-widget.md) | GET | Retrieves a recipe ingredients widget from Spoonacular. |
| [Ingredients Widget](actions/ingredients-widget.md) | GET | Generates a recipe ingredients widget in Spoonacular. |
| [Map Ingredients to Grocery Products](actions/map-ingredients-to-grocery-products.md) | GET | Maps ingredients to grocery products in Spoonacular. |
| [Menu Item Nutrition by ID Image](actions/menu-item-nutrition-by-id-image.md) | GET | Retrieves a menu item nutrition image from Spoonacular. |
| [Menu Item Nutrition by ID Widget](actions/menu-item-nutrition-by-id-widget.md) | GET | Retrieves a menu item nutrition widget from Spoonacular. |
| [Menu Item Nutrition Label Image](actions/menu-item-nutrition-label-image.md) | GET | Retrieves a menu item nutrition label image from Spoonacular. |
| [Menu Item Nutrition Label Widget](actions/menu-item-nutrition-label-widget.md) | GET | Retrieves a menu item nutrition label widget from Spoonacular. |
| [Nutrition by ID](actions/nutrition-by-id.md) | GET | Retrieves nutrition data for a Spoonacular recipe. |
| [Parse Ingredients](actions/parse-ingredients.md) | GET | Parses ingredient text in Spoonacular. |
| [Price Breakdown by ID](actions/price-breakdown-by-id.md) | GET | Retrieves price breakdown data for a Spoonacular recipe. |
| [Price Breakdown by ID Image](actions/price-breakdown-by-id-image.md) | GET | Retrieves a recipe price image from Spoonacular. |
| [Price Breakdown by ID Widget](actions/price-breakdown-by-id-widget.md) | GET | Retrieves a recipe price widget from Spoonacular. |
| [Price Breakdown Widget](actions/price-breakdown-widget.md) | GET | Generates a recipe price widget in Spoonacular. |
| [Product Nutrition by ID Image](actions/product-nutrition-by-id-image.md) | GET | Retrieves a product nutrition image from Spoonacular. |
| [Product Nutrition by ID Widget](actions/product-nutrition-by-id-widget.md) | GET | Retrieves a product nutrition widget from Spoonacular. |
| [Product Nutrition Label Image](actions/product-nutrition-label-image.md) | GET | Retrieves a product nutrition label image from Spoonacular. |
| [Product Nutrition Label Widget](actions/product-nutrition-label-widget.md) | GET | Retrieves a product nutrition label widget from Spoonacular. |
| [Quick Answer](actions/quick-answer.md) | GET | Retrieves a quick food answer from Spoonacular. |
| [Random Food Joke](actions/random-food-joke.md) | GET | Retrieves a random food joke from Spoonacular. |
| [Random Food Trivia](actions/random-food-trivia.md) | GET | Retrieves random food trivia from Spoonacular. |
| [Recipe Nutrition by ID Image](actions/recipe-nutrition-by-id-image.md) | GET | Retrieves a recipe nutrition image from Spoonacular. |
| [Recipe Nutrition by ID Widget](actions/recipe-nutrition-by-id-widget.md) | GET | Retrieves a recipe nutrition widget from Spoonacular. |
| [Recipe Nutrition Label Image](actions/recipe-nutrition-label-image.md) | GET | Retrieves a recipe nutrition label image from Spoonacular. |
| [Recipe Nutrition Label Widget](actions/recipe-nutrition-label-widget.md) | GET | Retrieves a recipe nutrition label widget from Spoonacular. |
| [Recipe Nutrition Widget](actions/recipe-nutrition-widget.md) | GET | Generates a recipe nutrition widget in Spoonacular. |
| [Recipe Taste by ID Image](actions/recipe-taste-by-id-image.md) | GET | Retrieves a recipe taste image from Spoonacular. |
| [Recipe Taste by ID Widget](actions/recipe-taste-by-id-widget.md) | GET | Retrieves a recipe taste widget from Spoonacular. |
| [Recipe Taste Widget](actions/recipe-taste-widget.md) | GET | Generates a recipe taste widget in Spoonacular. |
| [Search All Food](actions/search-all-food.md) | GET | Searches all food content in Spoonacular. |
| [Search Custom Foods](actions/search-custom-foods.md) | GET | Searches custom foods in Spoonacular. |
| [Search Food Videos](actions/search-food-videos.md) | GET | Searches food videos in Spoonacular. |
| [Search Grocery Products](actions/search-grocery-products.md) | GET | Searches grocery products in Spoonacular. |
| [Search Grocery Products by UPC](actions/search-grocery-products-by-upc.md) | GET | Retrieves a grocery product by UPC from Spoonacular. |
| [Search Menu Items](actions/search-menu-items.md) | GET | Searches menu items in Spoonacular. |
| [Search Recipes](actions/search-recipes.md) | GET | Searches Spoonacular recipes with advanced filters. |
| [Search Recipes by Ingredients](actions/search-recipes-by-ingredients.md) | GET | Finds Spoonacular recipes by available ingredients. |
| [Search Recipes by Nutrients](actions/search-recipes-by-nutrients.md) | GET | Finds Spoonacular recipes by nutrient limits. |
| [Search Restaurants](actions/search-restaurants.md) | GET | Searches for restaurants in Spoonacular. |
| [Search Site Content](actions/search-site-content.md) | GET | Searches Spoonacular site content by query. |
| [Summarize Recipe](actions/summarize-recipe.md) | GET | Retrieves a recipe summary from Spoonacular. |
| [Talk to Chatbot](actions/talk-to-chatbot.md) | GET | Retrieves a chatbot response from Spoonacular. |
| [Taste by ID](actions/taste-by-id.md) | GET | Retrieves taste data for a Spoonacular recipe. |
| [Wine Description](actions/wine-description.md) | GET | Retrieves a wine description from Spoonacular. |
| [Wine Pairing](actions/wine-pairing.md) | GET | Retrieves wine pairings for dishes from Spoonacular. |
| [Wine Recommendation](actions/wine-recommendation.md) | GET | Retrieves wine recommendations from Spoonacular. |

