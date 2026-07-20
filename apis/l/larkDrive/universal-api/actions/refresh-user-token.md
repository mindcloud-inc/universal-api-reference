# Lark Drive: Refresh User Token



```
PUT https://connect.mindcloud.co/v1/universal/larkDrive/latest/actions/refresh-user-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lark Drive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/larkDrive/latest/actions/refresh-user-token" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "refreshToken": "{{credentials.refreshToken}}"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/larkDrive/latest/actions/refresh-user-token', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "refreshToken": "{{credentials.refreshToken}}"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `refreshToken` | string | yes | Lark refresh_token. Lark rotates it on each refresh, so always persist and reuse the latest returned value. Default: `{{credentials.refreshToken}}`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "access_token": "string",
      "code": "string",
      "error": "string",
      "error_description": "string",
      "expires_in": 1,
      "refresh_token": "string",
      "refresh_token_expires_in": 1,
      "scope": "string",
      "token_type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `access_token` | string | User access token. |
| `code` | string | Lark response code. 0 means success. |
| `error` | string | OAuth error type when the request fails. |
| `error_description` | string | OAuth error details when the request fails. |
| `expires_in` | number | Access token lifetime in seconds. |
| `refresh_token` | string | New refresh token. Always persist the latest value. |
| `refresh_token_expires_in` | number | Refresh token lifetime in seconds. |
| `scope` | string | Granted scopes. |
| `token_type` | string | Bearer token type. |

## Native endpoint

Through the native Lark Drive API, this operation is `POST /authen/v2/oauth/token` (base URL `https://open.larksuite.com/open-apis`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/refresh-user-token.md) for the provider-specific parameters and requirements.

