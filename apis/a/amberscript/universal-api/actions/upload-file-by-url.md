# Amberscript: Upload File by URL

Uploads a file URL to create an Amberscript job.

```
POST https://connect.mindcloud.co/v1/universal/amberscript/latest/actions/upload-file-by-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Amberscript `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/amberscript/latest/actions/upload-file-by-url" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "sourceUrl": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/amberscript/latest/actions/upload-file-by-url', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "sourceUrl": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sourceUrl` | string | yes | Publicly accessible or presigned media URL. |
| `language` | string | no | Language code for the media. Use `auto` to let Amberscript detect supported languages automatically. Default: `en`. |
| `transcriptionType` | string | no | `transcription`, `captions`, or `translatedSubtitles`. Default: `transcription`. |
| `jobType` | string | no | `direct` for automatic jobs or `perfect` for manual jobs. Default: `direct`. |
| `numberOfSpeakers` | number | no | Known speaker count from `0` to `5`. Default: `2`. |
| `callbackUrl` | string | no | Optional webhook URL for final job status callbacks. |
| `glossaryId` | string | no | Optional glossary to apply to this upload. |
| `transcriptionStyle` | string | no | Transcript style: `cleanread` or `verbatim`. Default: `cleanread`. |
| `turnaroundTime` | string | no | Optional turnaround time for manual jobs. |
| `targetLanguage` | string | no | Target language code when requesting translated subtitles. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Amberscript API returns.

## Native endpoint

Through the native Amberscript API, this operation is `POST /jobs/upload-media-from-url` (base URL `https://api.amberscript.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-file-by-url.md) for the provider-specific parameters and requirements.

