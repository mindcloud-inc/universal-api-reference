# Ayrshare: Generate Profile JWT

Generates a single sign-on JWT in Ayrshare.

```
POST https://connect.mindcloud.co/v1/universal/ayrshare/latest/actions/generate-profile-jwt
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ayrshare `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/ayrshare/latest/actions/generate-profile-jwt" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "profileKey": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ayrshare/latest/actions/generate-profile-jwt', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "profileKey": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `profileKey` | string | yes | Profile key to generate a JWT linking URL for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "expiresIn": 1,
      "message": "string",
      "status": "string",
      "token": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number | Ayrshare error code. |
| `expiresIn` | number | Token expiry in seconds when returned. |
| `message` | string | JWT or error message. |
| `status` | string | JWT generation status. |
| `token` | string | Generated JWT token. |
| `url` | string | Generated social-linking URL. |

## Native endpoint

Through the native Ayrshare API, this operation is `POST /profiles/generateJWT` (base URL `https://api.ayrshare.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-profile-jwt.md) for the provider-specific parameters and requirements.

