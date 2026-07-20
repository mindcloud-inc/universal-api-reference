# Avoma: Get Recording By UUID

Retrieves a recording by UUID from Avoma.

```
GET https://connect.mindcloud.co/v1/universal/avoma/latest/actions/get-recording-by-uuid
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Avoma `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/avoma/latest/actions/get-recording-by-uuid?connectionId=$CONNECTION_ID&uuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "uuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/avoma/latest/actions/get-recording-by-uuid?${params}`, {
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
| `uuid` | string | yes | Unique ID of the recording. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "audio_url": "https://example.com",
      "meeting_uuid": "string",
      "uuid": "string",
      "valid_till": "2026-05-07T12:00:00.000Z",
      "video_url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `audio_url` | string |  |
| `meeting_uuid` | string |  |
| `uuid` | string |  |
| `valid_till` | date |  |
| `video_url` | string |  |

## Native endpoint

Through the native Avoma API, this operation is `GET /v1/recordings/:uuid/` (base URL `https://api.avoma.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-recording-by-uuid.md) for the provider-specific parameters and requirements.

