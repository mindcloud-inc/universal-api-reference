# Verbatik: Create Voice Clone

Creates a cloned voice in Verbatik.

```
POST https://connect.mindcloud.co/v1/universal/verbatik/latest/actions/create-voice-clone
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Verbatik `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/verbatik/latest/actions/create-voice-clone" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/verbatik/latest/actions/create-voice-clone', {
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
      "balance_cents": 1,
      "cost_cents": 1,
      "name": "Ava Chen",
      "preview_url": "https://example.com",
      "success": true,
      "voice_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `balance_cents` | number |  |
| `cost_cents` | number |  |
| `name` | string |  |
| `preview_url` | string |  |
| `success` | boolean |  |
| `voice_id` | string |  |

## Native endpoint

Through the native Verbatik API, this operation is `POST /v1/voice-training` (base URL `https://api.verbatik.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-voice-clone.md) for the provider-specific parameters and requirements.

