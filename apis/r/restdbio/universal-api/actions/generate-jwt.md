# Restdb.io: Generate JWT

Generates a JWT token in Restdb.io.

```
POST https://connect.mindcloud.co/v1/universal/restdbio/latest/actions/generate-jwt
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Restdb.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/restdbio/latest/actions/generate-jwt" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "payload": "string",
  "secret": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/restdbio/latest/actions/generate-jwt', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "payload": "string",
    "secret": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `payload` | string | yes | JSON object with JWT claims. |
| `secret` | string | yes | Path to the JWT secret configured in Restdb.io global settings. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Restdb.io API returns.

## Native endpoint

Through the native Restdb.io API, this operation is `POST /auth/jwt` (base URL `https://mindcloudstage0-7934.restdb.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-jwt.md) for the provider-specific parameters and requirements.

