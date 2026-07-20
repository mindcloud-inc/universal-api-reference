# Teachlr Organizations: Invite User And Subscribe To Courses



```
POST https://connect.mindcloud.co/v1/universal/teachlrOrganizations/latest/actions/invite-user-and-subscribe-to-courses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Teachlr Organizations `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/teachlrOrganizations/latest/actions/invite-user-and-subscribe-to-courses" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com",
  "courses[]": [
    1
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/teachlrOrganizations/latest/actions/invite-user-and-subscribe-to-courses', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com",
    "courses[]": [1]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes | Email address of the user to invite. |
| `courses[]` | array<number> | yes | List of active Teachlr course IDs to subscribe the invited user to. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Teachlr invitation result message. |

## Native endpoint

Through the native Teachlr Organizations API, this operation is `POST /invitations` (base URL `https://api.teachlr.com/mindcloudteachlr337933/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/invite-user-and-subscribe-to-courses.md) for the provider-specific parameters and requirements.

