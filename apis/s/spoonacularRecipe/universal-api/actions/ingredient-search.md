# Spoonacular Recipe: Ingredient Search

Finds whole-food ingredients in Spoonacular.

```
GET https://connect.mindcloud.co/v1/universal/spoonacularRecipe/latest/actions/ingredient-search
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Spoonacular Recipe `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/spoonacularRecipe/latest/actions/ingredient-search?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/spoonacularRecipe/latest/actions/ingredient-search?${params}`, {
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
      "name": "Ava Chen"
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
| `name` | string |  |

## Native endpoint

Through the native Spoonacular Recipe API, this operation is `GET /food/ingredients/search` (base URL `https://api.spoonacular.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/ingredient-search.md) for the provider-specific parameters and requirements.

