# Nutrient Document Web Services: Generate API Token

Creates an API token in Nutrient Document Web Services API.

```
POST https://connect.mindcloud.co/v1/universal/nutrientDocumentWebServicesAPI/latest/actions/generate-api-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nutrient Document Web Services `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/nutrientDocumentWebServicesAPI/latest/actions/generate-api-token" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/nutrientDocumentWebServicesAPI/latest/actions/generate-api-token', {
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
| `allowedOperations[]` | array<string> | no | Allowed operations for the token. |
| `allowedOrigins[]` | array<string> | no | Allowed origins for the token. |
| `expirationTime` | number | no | Token expiration time in seconds. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Nutrient Document Web Services API returns.

## Native endpoint

Through the native Nutrient Document Web Services API, this operation is `POST /tokens` (base URL `https://api.nutrient.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-api-token.md) for the provider-specific parameters and requirements.

