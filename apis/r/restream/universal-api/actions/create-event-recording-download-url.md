# Restream: Create Event Recording Download URL

Generates a download URL for an event recording in Restream.

```
GET https://connect.mindcloud.co/v1/universal/restream/latest/actions/create-event-recording-download-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Restream `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/restream/latest/actions/create-event-recording-download-url?connectionId=$CONNECTION_ID&eventId=string&fileName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "eventId": "string",
  "fileName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/restream/latest/actions/create-event-recording-download-url?${params}`, {
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
| `eventId` | string | yes | The UUID of the event whose recording download URL to generate. |
| `fileName` | string | yes | The file name from the event recordings response. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "downloadUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `downloadUrl` | string |  |

## Native endpoint

Through the native Restream API, this operation is `POST /user/events/:eventId/recordings/download-url` (base URL `https://api.restream.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-event-recording-download-url.md) for the provider-specific parameters and requirements.

