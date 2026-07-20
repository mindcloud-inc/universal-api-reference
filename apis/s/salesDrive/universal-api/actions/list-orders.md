# SalesDrive: List Orders

Retrieves a list of orders from SalesDrive.

```
GET https://connect.mindcloud.co/v1/universal/salesDrive/latest/actions/list-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SalesDrive `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/salesDrive/latest/actions/list-orders?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/salesDrive/latest/actions/list-orders?${params}`, {
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
| `updatedFrom` | string | no | Filter orders updated from this value. |
| `updatedTo` | string | no | Filter orders updated to this value. |
| `orderTimeFrom` | string | no | Filter orders by order time from this value. |
| `orderTimeTo` | string | no | Filter orders by order time to this value. |
| `statusId` | string | no | Filter orders by status ID. |
| `idFrom` | number | no | Filter orders with IDs from this value. |
| `idTo` | number | no | Filter orders with IDs to this value. |
| `organizationId` | number | no | Filter orders by organization ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "comment": "string",
      "contacts": [
        {}
      ],
      "externalId": "string",
      "formId": 1,
      "id": 1,
      "orderTime": "2026-05-07T12:00:00.000Z",
      "organizationId": 1,
      "payment_method": 1,
      "paymentAmount": 1,
      "primaryContact": {},
      "products": [
        {}
      ],
      "shipping_address": "string",
      "shipping_method": 1,
      "statusId": 1,
      "typeId": 1,
      "updateAt": "2026-05-07T12:00:00.000Z",
      "version": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `comment` | string |  |
| `contacts` | array<object> |  |
| `externalId` | string |  |
| `formId` | number |  |
| `id` | number |  |
| `orderTime` | date |  |
| `organizationId` | number |  |
| `payment_method` | number |  |
| `paymentAmount` | number |  |
| `primaryContact` | object |  |
| `products` | array<object> |  |
| `shipping_address` | string |  |
| `shipping_method` | number |  |
| `statusId` | number |  |
| `typeId` | number |  |
| `updateAt` | date |  |
| `version` | number |  |

## Native endpoint

Through the native SalesDrive API, this operation is `GET /api/order/list/` (base URL `https://{{credentials.account}}.salesdrive.me`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-orders.md) for the provider-specific parameters and requirements.

