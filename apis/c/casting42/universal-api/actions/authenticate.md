# Casting42: Authenticate

Creates a Casting42 authentication token from your API key.

```
POST https://connect.mindcloud.co/v1/universal/casting42/latest/actions/authenticate
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Casting42 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/casting42/latest/actions/authenticate" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/casting42/latest/actions/authenticate', {
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
      "accessToken": "string",
      "authenticated": true,
      "expiresIn": 1,
      "expiresOn": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accessToken` | string | Short-lived bearer token returned by Casting42 for normal API calls. |
| `authenticated` | boolean | Whether the Casting42 API key exchange succeeded. |
| `expiresIn` | number | Seconds until the exchanged bearer token expires when derivable from the Expiry header. |
| `expiresOn` | date | Parsed expiration timestamp from the Casting42 Expiry response header when available. |

## Native endpoint

Through the native Casting42 API, this operation is `POST /api/v2/auth` (base URL `https://casting42.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/authenticate.md) for the provider-specific parameters and requirements.

