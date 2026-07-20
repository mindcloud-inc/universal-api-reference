# BuildChatbot: Login

Creates a login session in BuildChatbot.

```
POST https://connect.mindcloud.co/v1/universal/buildChatbot/latest/actions/login
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BuildChatbot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/buildChatbot/latest/actions/login" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/buildChatbot/latest/actions/login', {
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
      "data": {
        "email": "ava@example.com",
        "msg": "string",
        "tenantId": "string",
        "token": "string",
        "userTenantBotCount": 1
      },
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.email` | string | Authenticated email. |
| `data.msg` | string | Login result message. |
| `data.tenantId` | string | Tenant identifier. |
| `data.token` | string | Bearer token returned by the provider. |
| `data.userTenantBotCount` | number | Current tenant bot count. |
| `status` | string | Provider response status. |

## Native endpoint

Through the native BuildChatbot API, this operation is `POST /login` (base URL `https://api.buildchatbot.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/login.md) for the provider-specific parameters and requirements.

