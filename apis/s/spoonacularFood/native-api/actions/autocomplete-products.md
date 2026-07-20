# Autocomplete Products with Spoonacular Food

Finds product suggestions in Spoonacular Food by partial name.

## Endpoint

- **Method:** `GET`
- **Path:** `/food/products/suggest`
- **Base URL:** `https://api.spoonacular.com`
- **Official documentation:** [Autocomplete Products](https://spoonacular.com/food-api/docs#Autocomplete-Product-Search)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | yes | Product name prefix to autocomplete. |
