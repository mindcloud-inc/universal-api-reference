# Get Wine Recommendation with Spoonacular Food

Retrieves wine recommendations from Spoonacular Food.

## Endpoint

- **Method:** `GET`
- **Path:** `/food/wine/recommendation`
- **Base URL:** `https://api.spoonacular.com`
- **Official documentation:** [Get Wine Recommendation](https://spoonacular.com/food-api/docs#Wine-Recommendation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `wine` | query | `string` | yes | Wine type to recommend products for. |
