# Spoonacular Recipe: Summarize Recipe

Retrieves a recipe summary from Spoonacular.

```
GET https://connect.mindcloud.co/v1/universal/spoonacularRecipe/latest/actions/summarize-recipe
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Spoonacular Recipe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/spoonacularRecipe/latest/actions/summarize-recipe?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/spoonacularRecipe/latest/actions/summarize-recipe?${params}`, {
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
      "id": 1,
      "summary": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `summary` | string |  |
| `title` | string |  |

## Native endpoint

Through the native Spoonacular Recipe API, this operation is `GET /recipes/{id}/summary` (base URL `https://api.spoonacular.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/summarize-recipe.md) for the provider-specific parameters and requirements.

