# EventGeek: Delete Event Contacts Export

Deletes an event contacts export from EventGeek.

```
DELETE https://connect.mindcloud.co/v1/universal/eventGeek/latest/actions/delete-event-contacts-export
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EventGeek `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/eventGeek/latest/actions/delete-event-contacts-export?connectionId=$CONNECTION_ID&event_id=RXZlbnQtNzg5NDE&export_id=78ac9d4f-a155-40f8-b335-067d159802df" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "event_id": "RXZlbnQtNzg5NDE",
  "export_id": "78ac9d4f-a155-40f8-b335-067d159802df"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eventGeek/latest/actions/delete-event-contacts-export?${params}`, {
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
| `export_id` | string | yes | Circa export identifier. Default: `78ac9d4f-a155-40f8-b335-067d159802df`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `message` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native EventGeek API, this operation is `DELETE /events/:event_id/contacts/exports/:export_id` (base URL `https://app.circa.co/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-event-contacts-export.md) for the provider-specific parameters and requirements.

