# Deepgram: Generate Temporary Token

Creates a temporary token in Deepgram.

```
POST https://connect.mindcloud.co/v1/universal/deepgram/latest/actions/generate-temporary-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Deepgram `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/deepgram/latest/actions/generate-temporary-token" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/deepgram/latest/actions/generate-temporary-token', {
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
| `ttlSeconds` | number | no | Time to live in seconds for the generated token. Example: `30`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accessToken": "string",
      "expiresIn": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accessToken` | string |  |
| `expiresIn` | number |  |

## Native endpoint

Through the native Deepgram API, this operation is `POST /v1/auth/grant` (base URL `https://api.deepgram.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-temporary-token.md) for the provider-specific parameters and requirements.

