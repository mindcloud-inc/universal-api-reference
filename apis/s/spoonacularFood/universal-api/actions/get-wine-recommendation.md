# Spoonacular Food: Get Wine Recommendation

Retrieves wine recommendations from Spoonacular Food.

```
GET https://connect.mindcloud.co/v1/universal/spoonacularFood/latest/actions/get-wine-recommendation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Spoonacular Food `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/spoonacularFood/latest/actions/get-wine-recommendation?connectionId=$CONNECTION_ID&wine=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "wine": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/spoonacularFood/latest/actions/get-wine-recommendation?${params}`, {
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
| `wine` | string | yes | Wine type to recommend products for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "id": 1,
      "price": "string",
      "rating": 1,
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `id` | number |  |
| `price` | string |  |
| `rating` | number |  |
| `title` | string |  |

## Native endpoint

Through the native Spoonacular Food API, this operation is `GET /food/wine/recommendation` (base URL `https://api.spoonacular.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-wine-recommendation.md) for the provider-specific parameters and requirements.

