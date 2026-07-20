# EasyPost: Buy Shipment

Purchases an existing shipment in EasyPost.

```
PUT https://connect.mindcloud.co/v1/universal/easyPost/latest/actions/buy-shipment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EasyPost `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/easyPost/latest/actions/buy-shipment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "rate": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/easyPost/latest/actions/buy-shipment', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "rate": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | EasyPost Shipment ID, beginning with shp_. |
| `rate` | object | yes | Selected EasyPost rate object or rate ID payload for buying the shipment. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "mode": "string",
      "object": "string",
      "postageLabel": {},
      "selectedRate": {},
      "status": "string",
      "tracker": {},
      "trackingCode": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `mode` | string |  |
| `object` | string |  |
| `postageLabel` | object |  |
| `selectedRate` | object |  |
| `status` | string |  |
| `tracker` | object |  |
| `trackingCode` | string |  |

## Native endpoint

Through the native EasyPost API, this operation is `POST /shipments/:id/buy` (base URL `https://api.easypost.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/buy-shipment.md) for the provider-specific parameters and requirements.

