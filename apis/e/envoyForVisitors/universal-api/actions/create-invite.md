# Envoy for Visitors: Create Invite

Creates a new invite in Envoy for Visitors.

```
POST https://connect.mindcloud.co/v1/universal/envoyForVisitors/latest/actions/create-invite
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Envoy for Visitors `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/envoyForVisitors/latest/actions/create-invite" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/envoyForVisitors/latest/actions/create-invite', {
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
      "approvalStatus": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "customFields": [
        {}
      ],
      "expectedArrivalAt": "2026-05-07T12:00:00.000Z",
      "expectedDepartureAt": "2026-05-07T12:00:00.000Z",
      "flowId": "string",
      "host": {},
      "id": "string",
      "invitee": {},
      "locationId": "string",
      "notes": "string",
      "photoUrl": "https://example.com",
      "recurringInviteId": "string",
      "secretToken": "string",
      "sendEmailToInvitee": true,
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
| `approvalStatus` | string |  |
| `createdAt` | date |  |
| `customFields` | array<object> |  |
| `expectedArrivalAt` | date |  |
| `expectedDepartureAt` | date |  |
| `flowId` | string |  |
| `host` | object |  |
| `id` | string |  |
| `invitee` | object |  |
| `locationId` | string |  |
| `notes` | string |  |
| `photoUrl` | string |  |
| `recurringInviteId` | string |  |
| `secretToken` | string |  |
| `sendEmailToInvitee` | boolean |  |
| `type` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Envoy for Visitors API, this operation is `POST /invites` (base URL `https://api.envoy.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-invite.md) for the provider-specific parameters and requirements.

