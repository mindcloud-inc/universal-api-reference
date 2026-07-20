# Rownd Data Privacy: Create Group Invite



```
POST https://connect.mindcloud.co/v1/universal/rowndDataPrivacy/latest/actions/create-group-invite
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rownd Data Privacy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rowndDataPrivacy/latest/actions/create-group-invite" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com",
  "group": "string",
  "roles[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rowndDataPrivacy/latest/actions/create-group-invite', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com",
    "group": "string",
    "roles[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes | Invitee email address. |
| `group` | string | yes | Rownd group identifier. |
| `redirect_url` | string | no | Redirect target for the invite link. |
| `roles[]` | array<string> | yes | Roles granted by the invite. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "email": "ava@example.com",
      "id": "string",
      "phone": "string",
      "roles": [
        "string"
      ],
      "state": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string | Invite email address when present. |
| `id` | string | Group invite identifier. |
| `phone` | string | Invite phone number when present. |
| `roles` | array<string> | Roles granted by the invite. |
| `state` | string | Invite state. |

## Native endpoint

Through the native Rownd Data Privacy API, this operation is `POST /groups/:group/invites` (base URL `https://api.rownd.io/applications/{{credentials.appId}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-group-invite.md) for the provider-specific parameters and requirements.

