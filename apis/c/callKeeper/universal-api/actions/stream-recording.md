# CallKeeper: Stream Recording

Retrieves a recording stream from CallKeeper.

```
GET https://connect.mindcloud.co/v1/universal/callKeeper/latest/actions/stream-recording
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CallKeeper `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/callKeeper/latest/actions/stream-recording?connectionId=$CONNECTION_ID&recordingId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "recordingId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/callKeeper/latest/actions/stream-recording?${params}`, {
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
| `recordingId` | string | yes | Recording identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "items": [
        {}
      ],
      "message": "string",
      "page": 1,
      "page_size": 1,
      "status": "string",
      "total": 1,
      "updated_at": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date | Creation timestamp. |
| `id` | string | Resource identifier. |
| `items` | array<object> | Returned collection items. |
| `message` | string | Status or result message. |
| `page` | number | Current page number. |
| `page_size` | number | Page size. |
| `status` | string | Resource or operation status. |
| `total` | number | Total result count. |
| `updated_at` | date | Last update timestamp. |
| `url` | string | Returned URL when available. |

## Native endpoint

Through the native CallKeeper API, this operation is `GET /recordings/:recording_id/stream` (base URL `https://api.callkeeper.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/stream-recording.md) for the provider-specific parameters and requirements.

