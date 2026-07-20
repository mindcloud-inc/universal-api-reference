# ElevenLabs: Create Single Use Token

Creates a single-use token in ElevenLabs.

```
POST https://connect.mindcloud.co/v1/universal/elevenLabs/latest/actions/create-single-use-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ElevenLabs `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/elevenLabs/latest/actions/create-single-use-token" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "tokenType": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/elevenLabs/latest/actions/create-single-use-token', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "tokenType": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `tokenType` | string | yes | The single-use token type. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ElevenLabs API returns.

## Native endpoint

Through the native ElevenLabs API, this operation is `POST /single-use-token/:token_type` (base URL `https://api.elevenlabs.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-single-use-token.md) for the provider-specific parameters and requirements.

