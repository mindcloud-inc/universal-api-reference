# Airzone Cloud: Refresh Session Token Pair

Creates a refreshed session token pair in Airzone Cloud.

```
POST https://connect.mindcloud.co/v1/universal/airzoneCloud/latest/actions/refresh-session-token-pair
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Airzone Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/airzoneCloud/latest/actions/refresh-session-token-pair" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "refreshToken": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/airzoneCloud/latest/actions/refresh-session-token-pair', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "refreshToken": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `refreshToken` | string | yes | Valid Airzone Cloud refresh token used to issue a new token pair. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "refreshToken": "string",
      "token": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `refreshToken` | string | New refresh token. |
| `token` | string | New JWT access token. |

## Native endpoint

Through the native Airzone Cloud API, this operation is `GET /auth/refreshToken/{refreshToken}` (base URL `https://m.airzonecloud.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/refresh-session-token-pair.md) for the provider-specific parameters and requirements.

