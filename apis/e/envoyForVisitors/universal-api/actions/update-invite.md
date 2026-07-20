# Envoy for Visitors: Update Invite

Updates an existing invite in Envoy for Visitors.

```
PUT https://connect.mindcloud.co/v1/universal/envoyForVisitors/latest/actions/update-invite
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Envoy for Visitors `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/envoyForVisitors/latest/actions/update-invite" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/envoyForVisitors/latest/actions/update-invite', {
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
| `id` | string | yes |  |

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

Through the native Envoy for Visitors API, this operation is `POST /invites/:id` (base URL `https://api.envoy.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-invite.md) for the provider-specific parameters and requirements.

