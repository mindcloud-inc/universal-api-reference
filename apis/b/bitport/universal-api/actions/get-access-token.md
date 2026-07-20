# Bitport: Get Access Token

Creates a Bitport access token from an access code.

```
POST https://connect.mindcloud.co/v1/universal/bitport/latest/actions/get-access-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bitport `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bitport/latest/actions/get-access-token" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bitport/latest/actions/get-access-token', {
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
      "access_token": "string",
      "expires_in": 1,
      "token_type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `access_token` | string | The Bitport access token. |
| `expires_in` | number | A long-lived expiration window used to avoid unnecessary re-authentication of manual Bitport access codes. |
| `token_type` | string | The token type returned for the access token. |

## Native endpoint

Through the native Bitport API, this operation is `POST /oauth2/access-token` (base URL `https://api.bitport.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-access-token.md) for the provider-specific parameters and requirements.

