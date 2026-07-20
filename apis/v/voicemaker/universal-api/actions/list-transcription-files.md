# Voicemaker: List Transcription Files

Retrieves all transcription files from Voicemaker.

```
GET https://connect.mindcloud.co/v1/universal/voicemaker/latest/actions/list-transcription-files
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Voicemaker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/voicemaker/latest/actions/list-transcription-files?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/voicemaker/latest/actions/list-transcription-files?${params}`, {
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
| `page` | number | no | Page number to return. |
| `limit` | number | no | Maximum number of transcription files to return. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "data": [
        {}
      ],
      "limit": "string",
      "page": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `data` | array<object> |  |
| `limit` | string |  |
| `page` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Voicemaker API, this operation is `GET api/v1/speech-to-text` (base URL `https://developer.voicemaker.in`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-transcription-files.md) for the provider-specific parameters and requirements.

