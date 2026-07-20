# Spoonacular Recipe: Get Ingredient Substitutes

Finds ingredient substitutes in Spoonacular by name.

```
GET https://connect.mindcloud.co/v1/universal/spoonacularRecipe/latest/actions/get-ingredient-substitutes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Spoonacular Recipe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/spoonacularRecipe/latest/actions/get-ingredient-substitutes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/spoonacularRecipe/latest/actions/get-ingredient-substitutes?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "ingredient": "string",
      "message": "string",
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
| `ingredient` | string |  |
| `message` | string |  |
| `substitutes` | array<string> |  |

## Native endpoint

Through the native Spoonacular Recipe API, this operation is `GET /food/ingredients/substitutes` (base URL `https://api.spoonacular.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-ingredient-substitutes.md) for the provider-specific parameters and requirements.

