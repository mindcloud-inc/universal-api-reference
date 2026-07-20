# Extensiv Order Manager: Get Order

Retrieves an order from Extensiv Order Manager.

```
GET https://connect.mindcloud.co/v1/universal/extensiv/latest/actions/get-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Extensiv Order Manager `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/extensiv/latest/actions/get-order?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/extensiv/latest/actions/get-order?${params}`, {
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
| `orderId` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "orderDate": "2026-05-07T12:00:00.000Z",
      "orderId": 1,
      "orderNumber": "string",
      "orderTotal": {},
      "salesChannelId": 1,
      "status": "string",
      "warehouseId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `orderDate` | date | Order date. |
| `orderId` | number | Order identifier. |
| `orderNumber` | string | Order number. |
| `orderTotal` | object | Order total amount object. |
| `salesChannelId` | number | Sales channel identifier. |
| `status` | string | Order status. |
| `warehouseId` | number | Warehouse identifier. |

## Native endpoint

Through the native Extensiv Order Manager API, this operation is `GET /v1.1/orders/:orderId` (base URL `https://api.skubana.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-order.md) for the provider-specific parameters and requirements.

