# AssemblyAI: Get Transcript Subtitles

Retrieves subtitle text for an AssemblyAI transcript.

```
GET https://connect.mindcloud.co/v1/universal/assemblyAI/latest/actions/get-transcript-subtitles
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AssemblyAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/assemblyAI/latest/actions/get-transcript-subtitles?connectionId=$CONNECTION_ID&transcriptId=string&subtitleFormat=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "transcriptId": "string",
  "subtitleFormat": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/assemblyAI/latest/actions/get-transcript-subtitles?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `transcriptId` | string | yes | The transcript ID to export subtitles for. |
| `subtitleFormat` | string | yes | Subtitle format to export. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `charsPerCaption` | number | no | Maximum characters per subtitle caption. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | string | Subtitle text payload returned by AssemblyAI. |

## Native endpoint

Through the native AssemblyAI API, this operation is `GET /v2/transcript/:transcript_id/:subtitle_format` (base URL `https://api.assemblyai.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-transcript-subtitles.md) for the provider-specific parameters and requirements.

