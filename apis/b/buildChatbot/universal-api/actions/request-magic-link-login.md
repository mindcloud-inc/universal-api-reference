# BuildChatbot: Request Magic Link Login

Requests a magic link login from BuildChatbot.

```
POST https://connect.mindcloud.co/v1/universal/buildChatbot/latest/actions/request-magic-link-login
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BuildChatbot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/buildChatbot/latest/actions/request-magic-link-login" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/buildChatbot/latest/actions/request-magic-link-login', {
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
        "detail": "string"
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
| `data.detail` | string | Magic link request result. |
| `status` | string | Provider response status. |

## Native endpoint

Through the native BuildChatbot API, this operation is `POST /login_with_magic_link` (base URL `https://api.buildchatbot.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/request-magic-link-login.md) for the provider-specific parameters and requirements.

