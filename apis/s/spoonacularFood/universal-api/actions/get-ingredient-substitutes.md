# Spoonacular Food: Get Ingredient Substitutes

Retrieves ingredient substitutes from Spoonacular Food.

```
GET https://connect.mindcloud.co/v1/universal/spoonacularFood/latest/actions/get-ingredient-substitutes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Spoonacular Food `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/spoonacularFood/latest/actions/get-ingredient-substitutes?connectionId=$CONNECTION_ID&ingredientName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ingredientName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/spoonacularFood/latest/actions/get-ingredient-substitutes?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `ingredientName` | string | yes | Ingredient to find substitutes for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ingredientName": "Ava Chen",
      "message": "string",
      "status": "string",
      "substitutes": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ingredientName` | string |  |
| `message` | string |  |
| `status` | string |  |
| `substitutes` | array<string> |  |

## Native endpoint

Through the native Spoonacular Food API, this operation is `GET /food/ingredients/substitutes` (base URL `https://api.spoonacular.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-ingredient-substitutes.md) for the provider-specific parameters and requirements.

