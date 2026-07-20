# EasyPost: Create Tracker

Creates a new tracker in EasyPost.

```
POST https://connect.mindcloud.co/v1/universal/easyPost/latest/actions/create-tracker
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EasyPost `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/easyPost/latest/actions/create-tracker" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "tracker": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/easyPost/latest/actions/create-tracker', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "tracker": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `tracker` | object | yes | Tracker object to create. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "carrier": "string",
      "id": "string",
      "mode": "string",
      "object": "string",
      "publicUrl": "https://example.com",
      "status": "string",
      "statusDetail": "string",
      "trackingCode": "string",
      "trackingDetails": [
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
| `carrier` | string |  |
| `id` | string |  |
| `mode` | string |  |
| `object` | string |  |
| `publicUrl` | string |  |
| `status` | string |  |
| `statusDetail` | string |  |
| `trackingCode` | string |  |
| `trackingDetails` | array<object> |  |

## Native endpoint

Through the native EasyPost API, this operation is `POST /trackers` (base URL `https://api.easypost.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-tracker.md) for the provider-specific parameters and requirements.

