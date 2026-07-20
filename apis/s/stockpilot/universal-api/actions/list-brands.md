# Stockpilot: List Brands

Retrieves brands from Stockpilot.

```
GET https://connect.mindcloud.co/v1/universal/stockpilot/latest/actions/list-brands
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stockpilot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stockpilot/latest/actions/list-brands?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stockpilot/latest/actions/list-brands?${params}`, {
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
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number | Stockpilot brand ID |
| `name` | string | Brand name |

## Native endpoint

Through the native Stockpilot API, this operation is `GET /brands` (base URL `https://api.stockpilot.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-brands.md) for the provider-specific parameters and requirements.

