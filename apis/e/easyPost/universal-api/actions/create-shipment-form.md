# EasyPost: Create Shipment Form

Creates a new shipment form in EasyPost.

```
POST https://connect.mindcloud.co/v1/universal/easyPost/latest/actions/create-shipment-form
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EasyPost `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/easyPost/latest/actions/create-shipment-form" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "form": {},
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/easyPost/latest/actions/create-shipment-form', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "form": {},
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `form` | object | yes | Form request details for the shipment. |
| `id` | string | yes | EasyPost Shipment ID, beginning with shp_. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "forms": [
        {}
      ],
      "id": "string",
      "messages": [
        {}
      ],
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
| `forms` | array<object> |  |
| `id` | string |  |
| `messages` | array<object> |  |
| `mode` | string |  |
| `object` | string |  |

## Native endpoint

Through the native EasyPost API, this operation is `POST /shipments/:id/forms` (base URL `https://api.easypost.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-shipment-form.md) for the provider-specific parameters and requirements.

