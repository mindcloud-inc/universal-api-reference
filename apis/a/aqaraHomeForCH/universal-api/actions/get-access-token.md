# Aqara Home for CH: Get Access Token

Creates Aqara access and refresh tokens from an authorization code.

```
POST https://connect.mindcloud.co/v1/universal/aqaraHomeForCH/latest/actions/get-access-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aqara Home for CH `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/aqaraHomeForCH/latest/actions/get-access-token" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "data": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/aqaraHomeForCH/latest/actions/get-access-token', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "data": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `data` | object | yes | Aqara request data object for the selected intent. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accessToken": "string",
      "expiresIn": "string",
      "openId": "string",
      "refreshToken": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accessToken` | string | Access token. |
| `expiresIn` | string | Remaining access-token lifetime in seconds. |
| `openId` | string | Authorized user's unique identifier. |
| `refreshToken` | string | Refresh token. |

## Native endpoint

Through the native Aqara Home for CH API, this operation is `POST /v3.0/open/api` (base URL `https://open-cn.aqara.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-access-token.md) for the provider-specific parameters and requirements.

