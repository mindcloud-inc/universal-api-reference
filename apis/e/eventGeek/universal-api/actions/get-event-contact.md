# EventGeek: Get Event Contact

Retrieves an event contact from EventGeek by ID.

```
GET https://connect.mindcloud.co/v1/universal/eventGeek/latest/actions/get-event-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EventGeek `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eventGeek/latest/actions/get-event-contact?connectionId=$CONNECTION_ID&contact_id=Q29udGFjdC0xOTA3MTc&event_id=RXZlbnQtNzg5NDE" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contact_id": "Q29udGFjdC0xOTA3MTc",
  "event_id": "RXZlbnQtNzg5NDE"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eventGeek/latest/actions/get-event-contact?${params}`, {
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
      "attendance_status": "string",
      "contact_id": "string",
      "email": "ava@example.com",
      "first_name": "Ava",
      "id": "string",
      "last_name": "Chen",
      "registration_status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attendance_status` | string |  |
| `contact_id` | string |  |
| `email` | string |  |
| `first_name` | string |  |
| `id` | string |  |
| `last_name` | string |  |
| `registration_status` | string |  |

## Native endpoint

Through the native EventGeek API, this operation is `GET /events/:event_id/contacts/:contact_id` (base URL `https://app.circa.co/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-event-contact.md) for the provider-specific parameters and requirements.

