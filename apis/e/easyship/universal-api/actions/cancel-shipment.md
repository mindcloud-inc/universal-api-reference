# Easyship: Cancel Shipment

Cancels a shipment in Easyship.

```
PUT https://connect.mindcloud.co/v1/universal/easyship/latest/actions/cancel-shipment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Easyship `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/easyship/latest/actions/cancel-shipment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "shipmentId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/easyship/latest/actions/cancel-shipment', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "shipmentId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `shipmentId` | string | yes | The Easyship shipment ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "meta": {
        "requestId": "string"
      },
      "success": {
        "message": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `meta.requestId` | string | Easyship request identifier. |
| `success.message` | string | Easyship cancellation result message. |

## Native endpoint

Through the native Easyship API, this operation is `POST /shipments/:shipment_id/cancel` (base URL `https://public-api.easyship.com/2024-09`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/cancel-shipment.md) for the provider-specific parameters and requirements.

