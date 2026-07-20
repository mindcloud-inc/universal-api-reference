# Spoonacular Recipe: Get Analyzed Recipe Instructions

Retrieves analyzed instructions for a Spoonacular recipe.

```
GET https://connect.mindcloud.co/v1/universal/spoonacularRecipe/latest/actions/get-analyzed-recipe-instructions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Spoonacular Recipe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/spoonacularRecipe/latest/actions/get-analyzed-recipe-instructions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/spoonacularRecipe/latest/actions/get-analyzed-recipe-instructions?${params}`, {
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
      "name": "Ava Chen",
      "steps": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `name` | string |  |
| `steps` | array<object> |  |

## Native endpoint

Through the native Spoonacular Recipe API, this operation is `GET /recipes/{id}/analyzedInstructions` (base URL `https://api.spoonacular.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-analyzed-recipe-instructions.md) for the provider-specific parameters and requirements.

