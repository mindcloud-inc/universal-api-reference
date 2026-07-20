# HeadshotPro: Create Invite

Creates a new invite in HeadshotPro.

```
POST https://connect.mindcloud.co/v1/universal/headshotPro/latest/actions/create-invite
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HeadshotPro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/headshotPro/latest/actions/create-invite" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/headshotPro/latest/actions/create-invite', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes | Email address to invite. |
| `teamId` | string | no | Optional team to assign when the invite is used. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "input": {},
      "link": "https://example.com",
      "message": "string",
      "success": true,
      "teamId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Created invite ID. |
| `input` | object | Echoed invite input. |
| `link` | string | Signed invite link. |
| `message` | string | Invite creation result message. |
| `success` | boolean | Whether the request succeeded. |
| `teamId` | string | Assigned team ID, when present. |

## Native endpoint

Through the native HeadshotPro API, this operation is `POST /organization/invites` (base URL `https://server.headshotpro.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-invite.md) for the provider-specific parameters and requirements.

