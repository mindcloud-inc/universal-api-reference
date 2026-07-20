# WEBLUCY: Start Member Session

Starts a member session in WEBLUCY.

```
POST https://connect.mindcloud.co/v1/universal/wEBLUCY/latest/actions/start-member-session
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WEBLUCY `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/wEBLUCY/latest/actions/start-member-session" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wEBLUCY/latest/actions/start-member-session', {
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
| `email` | string | yes | The member email address to start a session for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accessUrl": "https://example.com",
      "createdAt": 1,
      "expiresAt": 1,
      "token": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accessUrl` | string |  |
| `createdAt` | number |  |
| `expiresAt` | number |  |
| `token` | string |  |

## Native endpoint

Through the native WEBLUCY API, this operation is `POST /members/start-session` (base URL `https://apps.weblucy.com/api/site`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/start-member-session.md) for the provider-specific parameters and requirements.

