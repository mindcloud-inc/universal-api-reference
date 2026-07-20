# Avoma: Get Recording

Retrieves a recording for a meeting from Avoma.

```
GET https://connect.mindcloud.co/v1/universal/avoma/latest/actions/get-recording
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Avoma `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/avoma/latest/actions/get-recording?connectionId=$CONNECTION_ID&meetingUuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "meetingUuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/avoma/latest/actions/get-recording?${params}`, {
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
| `meetingUuid` | string | yes | Unique ID of the meeting. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "audioUrl": "https://example.com",
      "meetingUuid": "string",
      "uuid": "string",
      "validTill": "2026-05-07T12:00:00.000Z",
      "videoUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `audioUrl` | string |  |
| `meetingUuid` | string |  |
| `uuid` | string |  |
| `validTill` | date |  |
| `videoUrl` | string |  |

## Native endpoint

Through the native Avoma API, this operation is `GET /v1/recordings/` (base URL `https://api.avoma.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-recording.md) for the provider-specific parameters and requirements.

