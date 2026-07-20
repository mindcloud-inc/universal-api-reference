# Spoonacular Recipe: Extract Recipe from Website

Extracts recipe data from a website in Spoonacular.

```
GET https://connect.mindcloud.co/v1/universal/spoonacularRecipe/latest/actions/extract-recipe-from-website
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Spoonacular Recipe `connectionId` ([setup](../authentication.md)).

This action also supports [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/spoonacularRecipe/latest/actions/extract-recipe-from-website?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/spoonacularRecipe/latest/actions/extract-recipe-from-website?${params}`, {
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
      "image": "string",
      "readyInMinutes": 1,
      "servings": 1,
      "sourceUrl": "https://example.com",
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
| `image` | string |  |
| `readyInMinutes` | number |  |
| `servings` | number |  |
| `sourceUrl` | string |  |
| `title` | string |  |

## Native endpoint

Through the native Spoonacular Recipe API, this operation is `GET /recipes/extract` (base URL `https://api.spoonacular.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/extract-recipe-from-website.md) for the provider-specific parameters and requirements.

