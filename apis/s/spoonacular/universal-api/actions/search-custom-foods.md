# Spoonacular: Search Custom Foods

Searches custom foods in Spoonacular.

```
GET https://connect.mindcloud.co/v1/universal/spoonacular/latest/actions/search-custom-foods
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Spoonacular `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/spoonacular/latest/actions/search-custom-foods?connectionId=$CONNECTION_ID&hash=string&query=string&username=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "hash": "string",
  "query": "string",
  "username": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/spoonacular/latest/actions/search-custom-foods?${params}`, {
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
| `hash` | string | yes | Required by the Spoonacular endpoint. |
| `query` | string | yes | Required by the Spoonacular endpoint. |
| `username` | string | yes | Required by the Spoonacular endpoint. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "items": [
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
| `items` | array<object> |  |

## Native endpoint

Through the native Spoonacular API, this operation is `GET /food/customFoods/search` (base URL `https://api.spoonacular.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-custom-foods.md) for the provider-specific parameters and requirements.

