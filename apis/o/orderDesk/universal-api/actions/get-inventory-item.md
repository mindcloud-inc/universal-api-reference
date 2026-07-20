# Order Desk: Get Inventory Item

Retrieves an inventory item from Order Desk.

```
GET https://connect.mindcloud.co/v1/universal/orderDesk/latest/actions/get-inventory-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Order Desk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/orderDesk/latest/actions/get-inventory-item?connectionId=$CONNECTION_ID&inventoryItemId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "inventoryItemId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/orderDesk/latest/actions/get-inventory-item?${params}`, {
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
| `inventoryItemId` | string | yes | Order Desk internal inventory item ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "executionTime": "string",
      "initialRecordsReturned": 1,
      "inventoryItem": {},
      "recordsReturned": 1,
      "status": "string"
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
| `inventoryItem` | object |  |
| `recordsReturned` | number |  |
| `status` | string |  |

## Native endpoint

Through the native Order Desk API, this operation is `GET /inventory-items/:inventoryItemId` (base URL `https://app.orderdesk.me/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-inventory-item.md) for the provider-specific parameters and requirements.

