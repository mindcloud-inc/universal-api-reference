# CRUSH: Get Audio Download URL



```
GET https://connect.mindcloud.co/v1/universal/cRUSH/latest/actions/get-audio-download-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CRUSH `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cRUSH/latest/actions/get-audio-download-url?connectionId=$CONNECTION_ID&noteId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "noteId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cRUSH/latest/actions/get-audio-download-url?${params}`, {
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
| `noteId` | string | yes | The CRUSH note ID whose audio download URL should be returned. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "audioDurationSeconds": 1,
      "audioFormat": "string",
      "audioSizeBytes": 1,
      "audioUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `audioDurationSeconds` | number | Duration of the audio in seconds. |
| `audioFormat` | string | Audio container or file format. |
| `audioSizeBytes` | number | Size of the audio file in bytes. |
| `audioUrl` | string | Presigned download URL for the note audio. |

## Native endpoint

Through the native CRUSH API, this operation is `GET /aws/audio` (base URL `https://app.crushthememory.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-audio-download-url.md) for the provider-specific parameters and requirements.

