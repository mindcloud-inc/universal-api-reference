# Extensiv Order Manager: List Orders

Retrieves orders from Extensiv Order Manager.

```
GET https://connect.mindcloud.co/v1/universal/extensiv/latest/actions/list-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Extensiv Order Manager `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/extensiv/latest/actions/list-orders?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/extensiv/latest/actions/list-orders?${params}`, {
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
| `createdDateFrom` | string | no |  |
| `createdDateTo` | string | no |  |
| `external` | boolean | no |  |
| `modifiedDateFrom` | string | no |  |
| `modifiedDateTo` | string | no |  |
| `orderDateFrom` | string | no |  |
| `orderDateTo` | string | no |  |
| `orderId` | number | no |  |
| `orderNumber[]` | array<string> | no |  |
| `paymentDateFrom` | string | no |  |
| `paymentDateTo` | string | no |  |
| `productId[]` | array<number> | no |  |
| `salesChannelId` | number | no | Default: `0`. |
| `shipDateFrom` | string | no |  |
| `shipDateTo` | string | no |  |
| `status` | list<string> | no | Accepts multiple values as an array. |
| `unresolvedStatus` | list<string> | no | Accepts multiple values as an array. |
| `warehouseId` | number | no |  |

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

Through the native Extensiv Order Manager API, this operation is `GET /v1.1/orders` (base URL `https://api.skubana.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-orders.md) for the provider-specific parameters and requirements.

