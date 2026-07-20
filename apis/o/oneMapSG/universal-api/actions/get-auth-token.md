# OneMap SG: Get Auth Token

Creates an authentication token in OneMap SG.

```
POST https://connect.mindcloud.co/v1/universal/oneMapSG/latest/actions/get-auth-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OneMap SG `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/oneMapSG/latest/actions/get-auth-token" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/oneMapSG/latest/actions/get-auth-token', {
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
| `email` | string | no | The email address for your OneMap account. Default: `{{credentials.email}}`. Example: `name@example.com`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "access_token": "string",
      "expiry_timestamp": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `access_token` | string | The OneMap access token returned by the authentication endpoint. |
| `expiry_timestamp` | string | The token expiry timestamp returned by OneMap. |

## Native endpoint

Through the native OneMap SG API, this operation is `POST /api/auth/post/getToken` (base URL `https://www.onemap.gov.sg`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-auth-token.md) for the provider-specific parameters and requirements.

