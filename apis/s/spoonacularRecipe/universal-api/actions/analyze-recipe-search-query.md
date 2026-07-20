# Spoonacular Recipe: Analyze Recipe Search Query

Analyzes a recipe search query in Spoonacular.

```
GET https://connect.mindcloud.co/v1/universal/spoonacularRecipe/latest/actions/analyze-recipe-search-query
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Spoonacular Recipe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/spoonacularRecipe/latest/actions/analyze-recipe-search-query?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/spoonacularRecipe/latest/actions/analyze-recipe-search-query?${params}`, {
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
      "cuisines": [
        {}
      ],
      "dishes": [
        {}
      ],
      "ingredients": [
        {}
      ],
      "query": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cuisines` | array<object> |  |
| `dishes` | array<object> |  |
| `ingredients` | array<object> |  |
| `query` | string |  |

## Native endpoint

Through the native Spoonacular Recipe API, this operation is `GET /recipes/queries/analyze` (base URL `https://api.spoonacular.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/analyze-recipe-search-query.md) for the provider-specific parameters and requirements.

