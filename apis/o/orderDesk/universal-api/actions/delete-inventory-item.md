# Order Desk: Delete Inventory Item

Deletes an existing inventory item from Order Desk.

```
DELETE https://connect.mindcloud.co/v1/universal/orderDesk/latest/actions/delete-inventory-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Order Desk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/orderDesk/latest/actions/delete-inventory-item?connectionId=$CONNECTION_ID&inventoryItemId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "inventoryItemId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/orderDesk/latest/actions/delete-inventory-item?${params}`, {
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
      "message": "string",
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
| `message` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Order Desk API, this operation is `DELETE /inventory-items/:inventoryItemId` (base URL `https://app.orderdesk.me/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-inventory-item.md) for the provider-specific parameters and requirements.

