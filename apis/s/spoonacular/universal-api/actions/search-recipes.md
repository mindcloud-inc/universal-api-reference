# Spoonacular: Search Recipes

Searches Spoonacular recipes with advanced filters.

```
GET https://connect.mindcloud.co/v1/universal/spoonacular/latest/actions/search-recipes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Spoonacular `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/spoonacular/latest/actions/search-recipes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/spoonacular/latest/actions/search-recipes?${params}`, {
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
| `addRecipeNutrition` | string | no | Include recipe nutrition in the results. |
| `cuisine` | string | no | One or more cuisines, comma separated. |
| `diet` | string | no | Restrict recipes to a diet. |
| `number` | string | no | The number of recipes to return. |
| `offset` | string | no | How many matching recipes to skip. |
| `query` | string | no | The natural language recipe search query. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "number": 1,
      "offset": 1,
      "results": [
        {}
      ],
      "totalResults": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `number` | number | How many results were requested. |
| `offset` | number | How many matches were skipped. |
| `results` | array<object> | The matching recipes. |
| `totalResults` | number | The total number of matching recipes. |

## Native endpoint

Through the native Spoonacular API, this operation is `GET /recipes/complexSearch` (base URL `https://api.spoonacular.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-recipes.md) for the provider-specific parameters and requirements.

