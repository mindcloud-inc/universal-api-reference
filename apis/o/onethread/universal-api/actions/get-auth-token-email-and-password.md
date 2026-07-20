# Onethread: Get Auth Token (Email and Password)



```
POST https://connect.mindcloud.co/v1/universal/onethread/latest/actions/get-auth-token-email-and-password
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Onethread `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/onethread/latest/actions/get-auth-token-email-and-password" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/onethread/latest/actions/get-auth-token-email-and-password', {
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

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `username` | string | no | Default: `{{credentials.username}}`. |
| `password` | string | no | Default: `{{credentials.password}}`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accessToken": "string",
      "refreshToken": "string",
      "success": true,
      "user": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accessToken` | string |  |
| `refreshToken` | string |  |
| `success` | boolean |  |
| `user` | object |  |

## Native endpoint

Through the native Onethread API, this operation is `POST /accounts/login` (base URL `https://api.onethread.app/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-auth-token-email-and-password.md) for the provider-specific parameters and requirements.

