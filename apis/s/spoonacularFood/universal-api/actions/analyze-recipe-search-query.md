# Spoonacular Food: Analyze Recipe Search Query

Retrieves parsed recipe query details from Spoonacular Food.

```
GET https://connect.mindcloud.co/v1/universal/spoonacularFood/latest/actions/analyze-recipe-search-query
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Spoonacular Food `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/spoonacularFood/latest/actions/analyze-recipe-search-query?connectionId=$CONNECTION_ID&q=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "q": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/spoonacularFood/latest/actions/analyze-recipe-search-query?${params}`, {
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
| `q` | string | yes | Recipe search query to analyze. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cuisines": [
        "string"
      ],
      "dishes": [
        {}
      ],
      "ingredients": [
        {}
      ],
      "modifiers": [
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
| `cuisines` | array<string> |  |
| `dishes` | array<object> |  |
| `ingredients` | array<object> |  |
| `modifiers` | array<string> |  |

## Native endpoint

Through the native Spoonacular Food API, this operation is `GET /recipes/queries/analyze` (base URL `https://api.spoonacular.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/analyze-recipe-search-query.md) for the provider-specific parameters and requirements.

