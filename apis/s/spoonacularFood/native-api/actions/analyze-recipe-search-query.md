# Analyze Recipe Search Query with Spoonacular Food

Retrieves parsed recipe query details from Spoonacular Food.

## Endpoint

- **Method:** `GET`
- **Path:** `/recipes/queries/analyze`
- **Base URL:** `https://api.spoonacular.com`
- **Official documentation:** [Analyze Recipe Search Query](https://spoonacular.com/food-api/docs#Analyze-a-Recipe-Search-Query)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | yes | Recipe search query to analyze. |
