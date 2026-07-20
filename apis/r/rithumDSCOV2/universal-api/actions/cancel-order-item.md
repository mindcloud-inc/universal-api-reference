# Rithum DSCO: Cancel Order Item

Cancels an order item in Rithum DSCO.

```
PUT https://connect.mindcloud.co/v1/universal/rithumDSCOV2/latest/actions/cancel-order-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rithum DSCO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/rithumDSCOV2/latest/actions/cancel-order-item" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rithumDSCOV2/latest/actions/cancel-order-item', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "requestId": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `requestId` | string | DSCO request ID. |
| `status` | string | Cancellation status. |

## Native endpoint

Through the native Rithum DSCO API, this operation is `POST order/item/cancel` (base URL `https://api.dsco.io/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/cancel-order-item.md) for the provider-specific parameters and requirements.

