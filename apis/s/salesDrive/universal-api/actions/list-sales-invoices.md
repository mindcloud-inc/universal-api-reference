# SalesDrive: List Sales Invoices

Retrieves a list of sales invoices from SalesDrive.

```
GET https://connect.mindcloud.co/v1/universal/salesDrive/latest/actions/list-sales-invoices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SalesDrive `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/salesDrive/latest/actions/list-sales-invoices?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/salesDrive/latest/actions/list-sales-invoices?${params}`, {
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
      "addressDelivery": "string",
      "base": "string",
      "comment": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "date": "2026-05-07T12:00:00.000Z",
      "documentItems": [
        {}
      ],
      "id": 1,
      "nds": 1,
      "number": "string",
      "payerTypeId": 1,
      "responsibleId": 1,
      "token": "string",
      "totalSum": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "userId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addressDelivery` | string |  |
| `base` | string |  |
| `comment` | string |  |
| `createdAt` | date |  |
| `date` | date |  |
| `documentItems` | array<object> |  |
| `id` | number |  |
| `nds` | number |  |
| `number` | string |  |
| `payerTypeId` | number |  |
| `responsibleId` | number |  |
| `token` | string |  |
| `totalSum` | number |  |
| `updatedAt` | date |  |
| `userId` | number |  |

## Native endpoint

Through the native SalesDrive API, this operation is `GET /api/sales-invoice/list/` (base URL `https://{{credentials.account}}.salesdrive.me`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-sales-invoices.md) for the provider-specific parameters and requirements.

