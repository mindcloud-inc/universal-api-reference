# Spoonacular Food: Search All Food

Finds food content in Spoonacular Food by keyword.

```
GET https://connect.mindcloud.co/v1/universal/spoonacularFood/latest/actions/search-all-food
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Spoonacular Food `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/spoonacularFood/latest/actions/search-all-food?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/spoonacularFood/latest/actions/search-all-food?${params}`, {
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
| `query` | string | yes | Food search query. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "name": "Ava Chen",
      "results": [
        {}
      ],
      "totalResults": 1,
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `name` | string |  |
| `results` | array<object> |  |
| `totalResults` | number |  |
| `type` | string |  |

## Native endpoint

Through the native Spoonacular Food API, this operation is `GET /food/search` (base URL `https://api.spoonacular.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-all-food.md) for the provider-specific parameters and requirements.

