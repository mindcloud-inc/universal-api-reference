# EventGeek: Update Event Contact

Updates an event contact in EventGeek.

```
PUT https://connect.mindcloud.co/v1/universal/eventGeek/latest/actions/update-event-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EventGeek `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/eventGeek/latest/actions/update-event-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contact_id": "Q29udGFjdC0xOTA3MTc",
  "event_id": "RXZlbnQtNzg5NDE"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eventGeek/latest/actions/update-event-contact', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contact_id": "Q29udGFjdC0xOTA3MTc",
    "event_id": "RXZlbnQtNzg5NDE"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

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
      "event_id": "string",
      "id": "string",
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
| `event_id` | string |  |
| `id` | string |  |
| `registration_status` | string |  |

## Native endpoint

Through the native EventGeek API, this operation is `PATCH /events/:event_id/contacts/:contact_id` (base URL `https://app.circa.co/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-event-contact.md) for the provider-specific parameters and requirements.

