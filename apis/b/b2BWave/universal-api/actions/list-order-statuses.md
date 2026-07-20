# B2B Wave: List Order Statuses

Retrieves order statuses from B2B Wave.

```
GET https://connect.mindcloud.co/v1/universal/b2BWave/latest/actions/list-order-statuses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a B2B Wave `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/b2BWave/latest/actions/list-order-statuses?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/b2BWave/latest/actions/list-order-statuses?${params}`, {
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
      "is_temp": true,
      "name": "Ava Chen",
      "sort": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `is_temp` | boolean |  |
| `name` | string |  |
| `sort` | number |  |

## Native endpoint

Through the native B2B Wave API, this operation is `GET /status_orders/` (base URL `{{credentials.storeUrl}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-order-statuses.md) for the provider-specific parameters and requirements.

