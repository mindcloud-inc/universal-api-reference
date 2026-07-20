# Restream: Get Event

Retrieves an event from Restream by ID.

```
GET https://connect.mindcloud.co/v1/universal/restream/latest/actions/get-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Restream `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/restream/latest/actions/get-event?connectionId=$CONNECTION_ID&eventId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "eventId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/restream/latest/actions/get-event?${params}`, {
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
| `eventId` | string | yes | The UUID of the event to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "coverUrl": "https://example.com",
      "description": "string",
      "destinations": [
        {}
      ],
      "finishedAt": 1,
      "id": "string",
      "isRecordOnly": true,
      "scheduledFor": 1,
      "startedAt": 1,
      "status": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `coverUrl` | string |  |
| `description` | string |  |
| `destinations` | array<object> |  |
| `finishedAt` | number |  |
| `id` | string |  |
| `isRecordOnly` | boolean |  |
| `scheduledFor` | number |  |
| `startedAt` | number |  |
| `status` | string |  |
| `title` | string |  |

## Native endpoint

Through the native Restream API, this operation is `GET /user/events/:eventId` (base URL `https://api.restream.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-event.md) for the provider-specific parameters and requirements.

