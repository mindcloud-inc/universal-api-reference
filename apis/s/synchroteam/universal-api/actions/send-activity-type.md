# Synchroteam: Send Activity Type

Creates or updates an activity type in Synchroteam.

```
PUT https://connect.mindcloud.co/v1/universal/synchroteam/latest/actions/send-activity-type
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Synchroteam `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/synchroteam/latest/actions/send-activity-type" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "payload": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/synchroteam/latest/actions/send-activity-type', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "payload": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `payload` | object | yes | Request body payload for creating or updating an activity type (per docs). |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "data": {
        "color": "string",
        "hasConflit": true,
        "id": 1,
        "name": "Ava Chen"
      },
      "msg": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number |  |
| `data.color` | string |  |
| `data.hasConflit` | boolean |  |
| `data.id` | number |  |
| `data.name` | string |  |
| `msg` | string |  |

## Native endpoint

Through the native Synchroteam API, this operation is `POST /Api/V2/ActivityType/Send` (base URL `https://ws.synchroteam.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-activity-type.md) for the provider-specific parameters and requirements.

