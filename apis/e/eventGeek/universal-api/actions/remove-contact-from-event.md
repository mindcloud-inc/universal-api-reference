# EventGeek: Remove Contact From Event

Removes a contact from an event in EventGeek.

```
DELETE https://connect.mindcloud.co/v1/universal/eventGeek/latest/actions/remove-contact-from-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EventGeek `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/eventGeek/latest/actions/remove-contact-from-event?connectionId=$CONNECTION_ID&contact_id=Q29udGFjdC0xOTA3MTc&event_id=RXZlbnQtNzg5NDE" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contact_id": "Q29udGFjdC0xOTA3MTc",
  "event_id": "RXZlbnQtNzg5NDE"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eventGeek/latest/actions/remove-contact-from-event?${params}`, {
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
| `contact_id` | string | yes | Circa contact identifier. Default: `Q29udGFjdC0xOTA3MTc`. |
| `event_id` | string | yes | Circa event identifier. Default: `RXZlbnQtNzg5NDE`. |

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

Through the native EventGeek API, this operation is `DELETE /events/:event_id/contacts/:contact_id` (base URL `https://app.circa.co/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-contact-from-event.md) for the provider-specific parameters and requirements.

