# Sumtracker: List Purchase Orders or Stock Transfers

Retrieves purchase orders or stock transfers from Sumtracker.

```
GET https://connect.mindcloud.co/v1/universal/sumtracker/latest/actions/list-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sumtracker `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sumtracker/latest/actions/list-orders?connectionId=$CONNECTION_ID&limit=25&offset=0&document_type=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "document_type": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sumtracker/latest/actions/list-orders?${params}`, {
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
| `document_type` | string | yes | Use `orders` for purchase orders or `stock-transfers` for stock transfers. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "results": [
        {
          "number": "string",
          "reference": "string",
          "status": 1,
          "actionPerformed": "string",
          "isTaskInProgress": true,
          "currency": "string",
          "shipByTime": "2026-05-07T12:00:00.000Z",
          "created": "2026-05-07T12:00:00.000Z",
          "updated": "2026-05-07T12:00:00.000Z",
          "totalQuantity": 1,
          "totalAmount": "string",
          "totalTax": "string",
          "totalShipping": "string",
          "conversionRate": "string",
          "notes": "string",
          "id": 1,
          "contactId": 1,
          "warehouseId": 1,
          "fromWarehouseId": {}
        }
      ],
      "count": 1,
      "next": {},
      "previous": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `results[].number` | string |  |
| `results[].reference` | string |  |
| `results[].status` | number |  |
| `results[].actionPerformed` | string |  |
| `results[].isTaskInProgress` | boolean |  |
| `results[].currency` | string |  |
| `results[].shipByTime` | date |  |
| `results[].created` | date |  |
| `results[].updated` | date |  |
| `results[].totalQuantity` | number |  |
| `results[].totalAmount` | string |  |
| `results[].totalTax` | string |  |
| `results[].totalShipping` | string |  |
| `results[].conversionRate` | string |  |
| `results[].notes` | string |  |
| `results[].id` | number |  |
| `results[].contactId` | number |  |
| `results[].warehouseId` | number |  |
| `results[].fromWarehouseId` | object |  |
| `count` | number |  |
| `next` | object |  |
| `previous` | object |  |

## Native endpoint

Through the native Sumtracker API, this operation is `GET /api/version/2025-03/purchases/:document_type/` (base URL `https://inventory-api.sumtracker.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-orders.md) for the provider-specific parameters and requirements.

