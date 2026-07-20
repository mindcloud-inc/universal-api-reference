# Wine Pairing with Spoonacular

Retrieves wine pairings for dishes from Spoonacular.

## Endpoint

- **Method:** `GET`
- **Path:** `/food/wine/pairing`
- **Base URL:** `https://api.spoonacular.com`
- **Official documentation:** [Wine Pairing](https://spoonacular.com/food-api/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `food` | query | `string` | yes | Required by the Spoonacular endpoint. |
