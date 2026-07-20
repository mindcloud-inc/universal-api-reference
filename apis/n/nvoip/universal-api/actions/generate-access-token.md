# Nvoip: Generate Access Token



```
POST https://connect.mindcloud.co/v1/universal/nvoip/latest/actions/generate-access-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nvoip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/nvoip/latest/actions/generate-access-token" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "grantType": "string",
  "password": "string",
  "username": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/nvoip/latest/actions/generate-access-token', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "grantType": "string",
    "password": "string",
    "username": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `grantType` | string | yes | OAuth grant type documented by Nvoip for token generation. |
| `password` | string | yes | Paste the Nvoip User Token here to generate a fresh access token. |
| `username` | string | yes | Nvoip Numbersip or User SIP used to generate the access token. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "access_token": "string",
      "expires_in": 1,
      "refresh_token": "string",
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
| `access_token` | string | Bearer token returned by Nvoip for authenticated API calls. |
| `expires_in` | number | Seconds until the access token expires. |
| `refresh_token` | string | Refresh token returned by Nvoip. |
| `scope` | string | Granted scope string returned by Nvoip. |
| `token_type` | string | Token type returned by Nvoip. |

## Native endpoint

Through the native Nvoip API, this operation is `POST /oauth/token` (base URL `https://api.nvoip.com.br/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-access-token.md) for the provider-specific parameters and requirements.

