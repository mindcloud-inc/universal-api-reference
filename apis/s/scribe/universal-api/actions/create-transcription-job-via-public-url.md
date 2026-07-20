# 3Scribe: Create Transcription Job Via Public URL

Creates a new transcription job in 3Scribe from a public URL.

```
POST https://connect.mindcloud.co/v1/universal/scribe/latest/actions/create-transcription-job-via-public-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 3Scribe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/scribe/latest/actions/create-transcription-job-via-public-url" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/scribe/latest/actions/create-transcription-job-via-public-url', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | A descriptive title for the transcription job. |
| `url` | string | yes | A publicly accessible media URL that 3Scribe can download. |
| `language` | string | no | ISO language-country code for transcription, such as en-US. |
| `detectLanguage` | boolean | no | When true, 3Scribe detects the spoken language from the audio. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native 3Scribe API returns.

## Native endpoint

Through the native 3Scribe API, this operation is `POST /transcribe` (base URL `https://api.3scri.be`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-transcription-job-via-public-url.md) for the provider-specific parameters and requirements.

