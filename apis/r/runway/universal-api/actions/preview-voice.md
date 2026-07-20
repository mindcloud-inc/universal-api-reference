# Runway: Preview Voice

Creates a voice preview in Runway.

```
POST https://connect.mindcloud.co/v1/universal/runway/latest/actions/preview-voice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Runway `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/runway/latest/actions/preview-voice" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "model": "eleven_ttv_v3",
  "prompt": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/runway/latest/actions/preview-voice', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "model": "eleven_ttv_v3",
    "prompt": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `model` | string | yes | Voice design model, such as eleven_multilingual_ttv_v2 or eleven_ttv_v3. Default: `eleven_ttv_v3`. |
| `prompt` | string | yes | Voice description text, at least 20 characters. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "durationSecs": 1,
      "error": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `durationSecs` | number |  |
| `error` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Runway API, this operation is `POST /v1/voices/preview` (base URL `https://api.dev.runwayml.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/preview-voice.md) for the provider-specific parameters and requirements.

