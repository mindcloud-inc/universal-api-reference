# EasyPost: Rerate Shipment

Refreshes rates for an existing shipment in EasyPost.

```
PUT https://connect.mindcloud.co/v1/universal/easyPost/latest/actions/rerate-shipment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EasyPost `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/easyPost/latest/actions/rerate-shipment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/easyPost/latest/actions/rerate-shipment', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | EasyPost Shipment ID, beginning with shp_. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "messages": [
        {}
      ],
      "mode": "string",
      "object": "string",
      "rates": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `messages` | array<object> |  |
| `mode` | string |  |
| `object` | string |  |
| `rates` | array<object> |  |

## Native endpoint

Through the native EasyPost API, this operation is `POST /shipments/:id/rerate` (base URL `https://api.easypost.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/rerate-shipment.md) for the provider-specific parameters and requirements.

