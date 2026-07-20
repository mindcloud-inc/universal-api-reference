# Avoma: Get Transcription

Retrieves a transcription from Avoma.

```
GET https://connect.mindcloud.co/v1/universal/avoma/latest/actions/get-transcription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Avoma `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/avoma/latest/actions/get-transcription?connectionId=$CONNECTION_ID&uuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "uuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/avoma/latest/actions/get-transcription?${params}`, {
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
| `uuid` | string | yes | Unique ID of the transcription. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "meetingUuid": "string",
      "modified": "2026-05-07T12:00:00.000Z",
      "speakers": [
        {
          "email": "ava@example.com",
          "id": 1,
          "isRep": true,
          "name": "Ava Chen"
        }
      ],
      "transcript": [
        {
          "speakerId": 1,
          "timestamps": [
            1
          ],
          "transcript": "string"
        }
      ],
      "transcriptionVttUrl": "https://example.com",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `meetingUuid` | string |  |
| `modified` | date |  |
| `speakers[].email` | string |  |
| `speakers[].id` | number |  |
| `speakers[].isRep` | boolean |  |
| `speakers[].name` | string |  |
| `transcript[].speakerId` | number |  |
| `transcript[].timestamps[]` | number |  |
| `transcript[].transcript` | string |  |
| `transcriptionVttUrl` | string |  |
| `uuid` | string |  |

## Native endpoint

Through the native Avoma API, this operation is `GET /v1/transcriptions/:uuid/` (base URL `https://api.avoma.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-transcription.md) for the provider-specific parameters and requirements.

