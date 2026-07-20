# Envoy for Visitors: Create Recurring Invite

Creates a new recurring invite in Envoy for Visitors.

```
POST https://connect.mindcloud.co/v1/universal/envoyForVisitors/latest/actions/create-recurring-invite
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Envoy for Visitors `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/envoyForVisitors/latest/actions/create-recurring-invite" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/envoyForVisitors/latest/actions/create-recurring-invite', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "customFields": [
        {}
      ],
      "flowId": "string",
      "host": {},
      "id": "string",
      "invitee": {},
      "inviteIds": [
        "string"
      ],
      "locationId": "string",
      "notes": "string",
      "recurrenceRule": "string",
      "secretToken": "string",
      "sendEmailToInvitee": true,
      "startTime": "2026-05-07T12:00:00.000Z",
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `customFields` | array<object> |  |
| `flowId` | string |  |
| `host` | object |  |
| `id` | string |  |
| `invitee` | object |  |
| `inviteIds` | array<string> |  |
| `locationId` | string |  |
| `notes` | string |  |
| `recurrenceRule` | string |  |
| `secretToken` | string |  |
| `sendEmailToInvitee` | boolean |  |
| `startTime` | date |  |
| `type` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Envoy for Visitors API, this operation is `POST /recurring-invites` (base URL `https://api.envoy.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-recurring-invite.md) for the provider-specific parameters and requirements.

