# Dish Pairing for Wine with Spoonacular

Retrieves wine dish pairings from Spoonacular.

## Endpoint

- **Method:** `GET`
- **Path:** `/food/wine/dishes`
- **Base URL:** `https://api.spoonacular.com`
- **Official documentation:** [Dish Pairing for Wine](https://spoonacular.com/food-api/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `wine` | query | `string` | yes | Required by the Spoonacular endpoint. |
