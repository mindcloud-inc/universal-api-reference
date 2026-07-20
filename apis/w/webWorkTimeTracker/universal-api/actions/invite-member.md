# WebWork Time Tracker: Invite Member

Invites a new member to WebWork Time Tracker.

```
POST https://connect.mindcloud.co/v1/universal/webWorkTimeTracker/latest/actions/invite-member
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WebWork Time Tracker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/webWorkTimeTracker/latest/actions/invite-member" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workspaceId": 1,
  "email": "ava@example.com",
  "firstName": "Ava",
  "lastName": "Chen",
  "role": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/webWorkTimeTracker/latest/actions/invite-member', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workspaceId": 1,
    "email": "ava@example.com",
    "firstName": "Ava",
    "lastName": "Chen",
    "role": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workspaceId` | number | yes |  |
| `email` | string | yes |  |
| `firstName` | string | yes |  |
| `lastName` | string | yes |  |
| `role` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "invitationLink": "https://example.com",
      "userId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `invitationLink` | string |  |
| `userId` | number |  |

## Native endpoint

Through the native WebWork Time Tracker API, this operation is `POST /members` (base URL `https://api.webwork-tracker.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/invite-member.md) for the provider-specific parameters and requirements.

