# EventGeek: Create Event Contacts Export

Creates an event contacts export in EventGeek.

```
POST https://connect.mindcloud.co/v1/universal/eventGeek/latest/actions/create-event-contacts-export
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EventGeek `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/eventGeek/latest/actions/create-event-contacts-export" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "event_id": "RXZlbnQtNzg5NDE"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eventGeek/latest/actions/create-event-contacts-export', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "event_id": "RXZlbnQtNzg5NDE"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `event_id` | string | yes | Circa event identifier. Default: `RXZlbnQtNzg5NDE`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "string",
      "download_url": "https://example.com",
      "event_id": "string",
      "id": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | string |  |
| `download_url` | string |  |
| `event_id` | string |  |
| `id` | string |  |
| `status` | string |  |

## Native endpoint

Through the native EventGeek API, this operation is `POST /events/:event_id/contacts/exports` (base URL `https://app.circa.co/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-event-contacts-export.md) for the provider-specific parameters and requirements.

