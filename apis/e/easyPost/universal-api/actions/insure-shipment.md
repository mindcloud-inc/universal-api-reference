# EasyPost: Insure Shipment

Creates shipping insurance for a shipment in EasyPost.

```
PUT https://connect.mindcloud.co/v1/universal/easyPost/latest/actions/insure-shipment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EasyPost `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/easyPost/latest/actions/insure-shipment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "amount": "string",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/easyPost/latest/actions/insure-shipment', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "amount": "string",
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `amount` | string | yes | Insurance amount to add to the shipment. |
| `id` | string | yes | EasyPost Shipment ID, beginning with shp_. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "fees": [
        {}
      ],
      "id": "string",
      "insurance": "string",
      "mode": "string",
      "object": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fees` | array<object> |  |
| `id` | string |  |
| `insurance` | string |  |
| `mode` | string |  |
| `object` | string |  |

## Native endpoint

Through the native EasyPost API, this operation is `POST /shipments/:id/insure` (base URL `https://api.easypost.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/insure-shipment.md) for the provider-specific parameters and requirements.

