# Perplexity: Generate Auth Token

Creates an auth token in Perplexity.

```
POST https://connect.mindcloud.co/v1/universal/perplexity/latest/actions/generate-auth-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Perplexity `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/perplexity/latest/actions/generate-auth-token" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/perplexity/latest/actions/generate-auth-token', {
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
| `tokenName` | string | no | Example: `Production API Key`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "authToken": "string",
      "createdAtEpochSeconds": 1,
      "tokenName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `authToken` | string | The newly generated authentication token. |
| `createdAtEpochSeconds` | number | Unix timestamp when the token was created. |
| `tokenName` | string | The optional name associated with the token. |

## Native endpoint

Through the native Perplexity API, this operation is `POST /generate_auth_token` (base URL `https://api.perplexity.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-auth-token.md) for the provider-specific parameters and requirements.

