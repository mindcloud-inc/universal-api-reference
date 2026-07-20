# Verbatik: Create Custom Voice Speech

Creates speech from a cloned voice in Verbatik.

```
POST https://connect.mindcloud.co/v1/universal/verbatik/latest/actions/create-custom-voice-speech
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Verbatik `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/verbatik/latest/actions/create-custom-voice-speech" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/verbatik/latest/actions/create-custom-voice-speech', {
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

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Verbatik API returns.

## Native endpoint

Through the native Verbatik API, this operation is `POST /v1/voice-cloning` (base URL `https://api.verbatik.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-custom-voice-speech.md) for the provider-specific parameters and requirements.

