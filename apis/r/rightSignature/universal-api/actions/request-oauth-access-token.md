# RightSignature: Request OAuth Access Token

Requests a RightSignature OAuth access token.

```
POST https://connect.mindcloud.co/v1/universal/rightSignature/latest/actions/request-oauth-access-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RightSignature `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rightSignature/latest/actions/request-oauth-access-token" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "clientId": "string",
  "clientSecret": "string",
  "redirectUri": "string",
  "code": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rightSignature/latest/actions/request-oauth-access-token', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "clientId": "string",
    "clientSecret": "string",
    "redirectUri": "string",
    "code": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `clientId` | string | yes | The API Key's Client ID |
| `clientSecret` | string | yes | The API Key's Client Secret |
| `redirectUri` | string | yes | The API Key's redirect uri that was used in the authorization grant request |
| `code` | string | yes | The code that was included as a param in the redirect after authorizing |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accessToken": "string",
      "createdAt": 1,
      "expiresIn": 1,
      "refreshToken": "string",
      "scope": "string",
      "tokenType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accessToken` | string |  |
| `createdAt` | number |  |
| `expiresIn` | number |  |
| `refreshToken` | string |  |
| `scope` | string |  |
| `tokenType` | string |  |

## Native endpoint

Through the native RightSignature API, this operation is `POST https://api.rightsignature.com/oauth/token` (base URL `https://api.rightsignature.com/public/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/request-oauth-access-token.md) for the provider-specific parameters and requirements.

