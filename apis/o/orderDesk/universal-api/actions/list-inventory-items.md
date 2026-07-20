# Order Desk: List Inventory Items

Retrieves inventory items from Order Desk.

```
GET https://connect.mindcloud.co/v1/universal/orderDesk/latest/actions/list-inventory-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Order Desk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/orderDesk/latest/actions/list-inventory-items?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/orderDesk/latest/actions/list-inventory-items?${params}`, {
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
| `code` | string | no | Filter inventory items by SKU code. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "executionTime": "string",
      "initialRecordsReturned": 1,
      "inventoryItems": [
        {}
      ],
      "recordsReturned": 1,
      "status": "string",
      "totalRecords": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `executionTime` | string |  |
| `initialRecordsReturned` | number |  |
| `inventoryItems` | array<object> |  |
| `recordsReturned` | number |  |
| `status` | string |  |
| `totalRecords` | string |  |

## Native endpoint

Through the native Order Desk API, this operation is `GET /inventory-items` (base URL `https://app.orderdesk.me/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-inventory-items.md) for the provider-specific parameters and requirements.

