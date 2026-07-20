# EasyPost: Create Pickup

Creates a new pickup in EasyPost.

```
POST https://connect.mindcloud.co/v1/universal/easyPost/latest/actions/create-pickup
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EasyPost `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/easyPost/latest/actions/create-pickup" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "pickup": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/easyPost/latest/actions/create-pickup', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "pickup": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `pickup` | object | yes | Pickup object to create. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "confirmation": "string",
      "id": "string",
      "maxDatetime": "2026-05-07T12:00:00.000Z",
      "minDatetime": "2026-05-07T12:00:00.000Z",
      "mode": "string",
      "object": "string",
      "pickupRates": [
        {}
      ],
      "reference": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `confirmation` | string |  |
| `id` | string |  |
| `maxDatetime` | date |  |
| `minDatetime` | date |  |
| `mode` | string |  |
| `object` | string |  |
| `pickupRates` | array<object> |  |
| `reference` | string |  |
| `status` | string |  |

## Native endpoint

Through the native EasyPost API, this operation is `POST /pickups` (base URL `https://api.easypost.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-pickup.md) for the provider-specific parameters and requirements.

