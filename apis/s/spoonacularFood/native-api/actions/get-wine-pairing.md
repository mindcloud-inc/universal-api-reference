# Get Wine Pairing with Spoonacular Food

Retrieves wine pairings from Spoonacular Food for a dish.

## Endpoint

- **Method:** `GET`
- **Path:** `/food/wine/pairing`
- **Base URL:** `https://api.spoonacular.com`
- **Official documentation:** [Get Wine Pairing](https://spoonacular.com/food-api/docs#Wine-Pairing)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `food` | query | `string` | yes | Dish, cuisine, or ingredient to pair with wine. |
