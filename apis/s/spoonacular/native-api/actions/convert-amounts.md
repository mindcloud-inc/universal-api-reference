# Convert Amounts with Spoonacular

Converts ingredient amounts in Spoonacular.

## Endpoint

- **Method:** `GET`
- **Path:** `/recipes/convert`
- **Base URL:** `https://api.spoonacular.com`
- **Official documentation:** [Convert Amounts](https://spoonacular.com/food-api/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ingredientName` | query | `string` | yes | Required by the Spoonacular endpoint. |
| `sourceAmount` | query | `string` | yes | Required by the Spoonacular endpoint. |
| `sourceUnit` | query | `string` | yes | Required by the Spoonacular endpoint. |
| `targetUnit` | query | `string` | yes | Required by the Spoonacular endpoint. |
