# Pachca (Admin): Set Current Status

Updates your current status in the Pachca Admin API.

```
PUT https://connect.mindcloud.co/v1/universal/pachcaAdmin/latest/actions/set-user-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pachca (Admin) `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/pachcaAdmin/latest/actions/set-user-status" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "status.emoji": "string",
  "status.title": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pachcaAdmin/latest/actions/set-user-status', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "status.emoji": "string",
    "status.title": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `status.emoji` | string | yes |  |
| `status.title` | string | yes |  |
| `status.expiresAt` | date | no |  |
| `status.isAway` | boolean | no |  |
| `status.awayMessage` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "awayMessage": {
          "text": "string"
        },
        "emoji": "string",
        "expiresAt": {},
        "isAway": true,
        "title": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.awayMessage.text` | string |  |
| `data.emoji` | string |  |
| `data.expiresAt` | object |  |
| `data.isAway` | boolean |  |
| `data.title` | string |  |

## Native endpoint

Through the native Pachca (Admin) API, this operation is `PUT /profile/status` (base URL `https://api.pachca.com/api/shared/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/set-user-status.md) for the provider-specific parameters and requirements.

