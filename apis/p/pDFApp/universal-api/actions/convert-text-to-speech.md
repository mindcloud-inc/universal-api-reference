# PDF-app: Convert Text To Speech

Creates speech audio from text in PDF-app.

```
POST https://connect.mindcloud.co/v1/universal/pDFApp/latest/actions/convert-text-to-speech
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PDF-app `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pDFApp/latest/actions/convert-text-to-speech" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pDFApp/latest/actions/convert-text-to-speech', {
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
| `fileUrl` | string | no | Optional text file or HTML file URL to convert to speech. Example: `https://example.com/input.txt`. |
| `text` | string | no | Plain text or SSML content to convert to speech. Example: `Hello from MindCloud`. |
| `voiceId` | string | no | AWS Polly voice identifier to use for the generated audio. Example: `Danielle`. |
| `outputFormat` | string | no | Audio output format, such as mp3 or ogg_vorbis. Example: `mp3`. |
| `async` | boolean | no | Whether to run speech generation asynchronously. Default: `false`. |
| `type` | string | no | Speech engine type: longform, generative, neural, or standard. Example: `standard`. |
| `language` | string | no | Language code for the selected voice. Example: `en-US`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "creditsConsumed": 1,
      "creditsRemaining": 1,
      "job_id": "string",
      "message": "string",
      "presignedUrl": [
        "https://example.com"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `creditsConsumed` | number | Credits consumed by the request. |
| `creditsRemaining` | number | Remaining provider credits after the request. |
| `job_id` | string | Provider job identifier for the text-to-speech request. |
| `message` | string | Summary of the speech conversion result. |
| `presignedUrl` | array<string> | Temporary download URLs for the generated audio output. |

## Native endpoint

Through the native PDF-app API, this operation is `POST /text_to_voice` (base URL `https://api.pdf-app.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/convert-text-to-speech.md) for the provider-specific parameters and requirements.

