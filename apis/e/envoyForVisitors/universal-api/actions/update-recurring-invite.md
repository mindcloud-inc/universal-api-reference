# Envoy for Visitors: Update Recurring Invite

Updates an existing recurring invite in Envoy for Visitors.

```
PUT https://connect.mindcloud.co/v1/universal/envoyForVisitors/latest/actions/update-recurring-invite
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Envoy for Visitors `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/envoyForVisitors/latest/actions/update-recurring-invite" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/envoyForVisitors/latest/actions/update-recurring-invite', {
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

Through the native Envoy for Visitors API, this operation is `POST /recurring-invites/:id` (base URL `https://api.envoy.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-recurring-invite.md) for the provider-specific parameters and requirements.

