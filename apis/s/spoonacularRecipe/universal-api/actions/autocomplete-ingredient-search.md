# Spoonacular Recipe: Autocomplete Ingredient Search

Finds ingredient name completions in Spoonacular.

```
GET https://connect.mindcloud.co/v1/universal/spoonacularRecipe/latest/actions/autocomplete-ingredient-search
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Spoonacular Recipe `connectionId` ([setup](../authentication.md)).

This action also supports [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/spoonacularRecipe/latest/actions/autocomplete-ingredient-search?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/spoonacularRecipe/latest/actions/autocomplete-ingredient-search?${params}`, {
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
      "aisle": "string",
      "id": 1,
      "image": "string",
      "name": "Ava Chen",
      "possibleUnits": [
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
| `aisle` | string |  |
| `id` | number |  |
| `image` | string |  |
| `name` | string |  |
| `possibleUnits` | array<string> |  |

## Native endpoint

Through the native Spoonacular Recipe API, this operation is `GET /food/ingredients/autocomplete` (base URL `https://api.spoonacular.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/autocomplete-ingredient-search.md) for the provider-specific parameters and requirements.

