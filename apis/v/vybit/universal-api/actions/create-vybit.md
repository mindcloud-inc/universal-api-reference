# Vybit: Create Vybit



```
POST https://connect.mindcloud.co/v1/universal/vybit/latest/actions/create-vybit
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vybit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/vybit/latest/actions/create-vybit" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vybit/latest/actions/create-vybit', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `access` | string | no | Vybit visibility and access control |
| `description` | string | no | Detailed vybit description |
| `imageUrl` | string | no | Default image URL for notifications |
| `linkUrl` | string | no | Default link URL for notifications |
| `message` | string | no | Default notification message |
| `name` | string | yes | Vybit display name |
| `sendPermissions` | string | no | Who can trigger and receive notifications |
| `soundKey` | string | no | Sound key from the Sounds endpoint |
| `status` | string | no | Vybit status |
| `triggerType` | string | no | How the vybit is triggered |

## Response

```json
{
  "success": true,
  "data": [
    {
      "access": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "following": true,
      "geofence": {},
      "imageUrl": "https://example.com",
      "key": "string",
      "linkUrl": "https://example.com",
      "message": "string",
      "name": "Ava Chen",
      "numberFollowers": 1,
      "sendPermissions": "string",
      "soundKey": "string",
      "status": "string",
      "subscriptionKey": "string",
      "triggerKey": "string",
      "triggerSettings": {},
      "triggerType": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `access` | string |  |
| `createdAt` | date |  |
| `description` | string |  |
| `following` | boolean |  |
| `geofence` | object |  |
| `imageUrl` | string |  |
| `key` | string |  |
| `linkUrl` | string |  |
| `message` | string |  |
| `name` | string |  |
| `numberFollowers` | number |  |
| `sendPermissions` | string |  |
| `soundKey` | string |  |
| `status` | string |  |
| `subscriptionKey` | string |  |
| `triggerKey` | string |  |
| `triggerSettings` | object |  |
| `triggerType` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Vybit API, this operation is `POST /vybit` (base URL `https://api.vybit.net/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-vybit.md) for the provider-specific parameters and requirements.

