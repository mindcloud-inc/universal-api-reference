# Wine Recommendation with Spoonacular

Retrieves wine recommendations from Spoonacular.

## Endpoint

- **Method:** `GET`
- **Path:** `/food/wine/recommendation`
- **Base URL:** `https://api.spoonacular.com`
- **Official documentation:** [Wine Recommendation](https://spoonacular.com/food-api/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `wine` | query | `string` | yes | Required by the Spoonacular endpoint. |
