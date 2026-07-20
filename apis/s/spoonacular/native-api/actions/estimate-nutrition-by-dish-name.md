# Estimate Nutrition by Dish Name with Spoonacular

Estimates nutrition for a dish name in Spoonacular.

## Endpoint

- **Method:** `GET`
- **Path:** `/recipes/guessNutrition`
- **Base URL:** `https://api.spoonacular.com`
- **Official documentation:** [Estimate Nutrition by Dish Name](https://spoonacular.com/food-api/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | query | `string` | yes | Required by the Spoonacular endpoint. |
