# TrackMage: Lookup Order

Finds an order in TrackMage by search criteria.

```
GET https://connect.mindcloud.co/v1/universal/trackMage/latest/actions/lookup-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TrackMage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/trackMage/latest/actions/lookup-order?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/trackMage/latest/actions/lookup-order?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workspaceId` | string | no |  |
| `search` | string | no |  |
| `shipmentId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "orders": {
        "id": "string",
        "orderNumber": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `orders` | array<object> |  |
| `orders.id` | string |  |
| `orders.orderNumber` | string |  |

## Native endpoint

Through the native TrackMage API, this operation is `POST /orders/lookup` (base URL `https://api.trackmage.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/lookup-order.md) for the provider-specific parameters and requirements.

