# Restream: Get Event Stream Key

Retrieves an event stream key from Restream.

```
GET https://connect.mindcloud.co/v1/universal/restream/latest/actions/get-event-stream-key
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Restream `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/restream/latest/actions/get-event-stream-key?connectionId=$CONNECTION_ID&eventId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "eventId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/restream/latest/actions/get-event-stream-key?${params}`, {
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
| `eventId` | string | yes | The UUID of the event whose stream key to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "srtUrl": "https://example.com",
      "streamKey": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `srtUrl` | string |  |
| `streamKey` | string |  |

## Native endpoint

Through the native Restream API, this operation is `GET /user/events/:eventId/streamKey` (base URL `https://api.restream.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-event-stream-key.md) for the provider-specific parameters and requirements.

