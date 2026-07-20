# EasyPost: Create Shipment

Creates a new shipment in EasyPost.

```
POST https://connect.mindcloud.co/v1/universal/easyPost/latest/actions/create-shipment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EasyPost `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/easyPost/latest/actions/create-shipment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "shipment": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/easyPost/latest/actions/create-shipment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "shipment": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `shipment` | object | yes | Shipment object to create. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "mode": "string",
      "object": "string",
      "postageLabel": {},
      "rates": [
        {}
      ],
      "selectedRate": {},
      "status": "string",
      "tracker": {},
      "trackingCode": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date | Creation timestamp. |
| `id` | string | EasyPost Shipment ID. |
| `mode` | string | EasyPost mode. |
| `object` | string | EasyPost object type. |
| `postageLabel` | object | Shipment postage label. |
| `rates` | array<object> | Available shipment rates. |
| `selectedRate` | object | Purchased or selected rate. |
| `status` | string | Shipment status. |
| `tracker` | object | Associated tracker. |
| `trackingCode` | string | Shipment tracking code. |
| `updatedAt` | date | Last update timestamp. |

## Native endpoint

Through the native EasyPost API, this operation is `POST /shipments` (base URL `https://api.easypost.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-shipment.md) for the provider-specific parameters and requirements.

