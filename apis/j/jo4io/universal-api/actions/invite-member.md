# jo4.io: Invite Member



```
POST https://connect.mindcloud.co/v1/universal/jo4io/latest/actions/invite-member
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a jo4.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/jo4io/latest/actions/invite-member" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com",
  "teamSlug": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/jo4io/latest/actions/invite-member', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com",
    "teamSlug": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes |  |
| `role` | string | no |  |
| `teamSlug` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "acceptedAt": 1,
      "createdTime": 1,
      "email": "ava@example.com",
      "expiresAt": 1,
      "id": 1,
      "invitedBy": 1,
      "invitedByEmail": "ava@example.com",
      "role": "string",
      "slug": "string",
      "status": "string",
      "teamId": 1,
      "teamName": "Ava Chen",
      "teamSlug": "string",
      "token": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `acceptedAt` | number |  |
| `createdTime` | number |  |
| `email` | string |  |
| `expiresAt` | number |  |
| `id` | number |  |
| `invitedBy` | number |  |
| `invitedByEmail` | string |  |
| `role` | string |  |
| `slug` | string |  |
| `status` | string |  |
| `teamId` | number |  |
| `teamName` | string |  |
| `teamSlug` | string |  |
| `token` | string |  |

## Native endpoint

Through the native jo4.io API, this operation is `POST /protected/teams/:teamSlug/invitations` (base URL `https://jo4-api.jo4.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/invite-member.md) for the provider-specific parameters and requirements.

