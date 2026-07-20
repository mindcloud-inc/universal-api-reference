# EventGeek: Get Event Contacts Export

Retrieves an event contacts export from EventGeek.

```
GET https://connect.mindcloud.co/v1/universal/eventGeek/latest/actions/get-event-contacts-export
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EventGeek `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eventGeek/latest/actions/get-event-contacts-export?connectionId=$CONNECTION_ID&event_id=RXZlbnQtNzg5NDE&export_id=0f0f7bec-79a5-4a20-80e5-4ffaf759ef0e" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "event_id": "RXZlbnQtNzg5NDE",
  "export_id": "0f0f7bec-79a5-4a20-80e5-4ffaf759ef0e"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eventGeek/latest/actions/get-event-contacts-export?${params}`, {
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
| `event_id` | string | yes | Circa event identifier. Default: `RXZlbnQtNzg5NDE`. |
| `export_id` | string | yes | Circa export identifier. Default: `0f0f7bec-79a5-4a20-80e5-4ffaf759ef0e`. |

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

Through the native EventGeek API, this operation is `GET /events/:event_id/contacts/exports/:export_id` (base URL `https://app.circa.co/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-event-contacts-export.md) for the provider-specific parameters and requirements.

