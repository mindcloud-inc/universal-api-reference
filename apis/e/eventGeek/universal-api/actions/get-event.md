# EventGeek: Get Event

Retrieves an event from EventGeek by ID.

```
GET https://connect.mindcloud.co/v1/universal/eventGeek/latest/actions/get-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EventGeek `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eventGeek/latest/actions/get-event?connectionId=$CONNECTION_ID&event_id=RXZlbnQtNzg5NDE" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "event_id": "RXZlbnQtNzg5NDE"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eventGeek/latest/actions/get-event?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "custom_fields": {},
      "end_date": "string",
      "id": "string",
      "location": "string",
      "name": "Ava Chen",
      "roles": [
        "string"
      ],
      "start_date": "string",
      "status": "string",
      "team_id": "string",
      "types": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `custom_fields` | object |  |
| `end_date` | string |  |
| `id` | string |  |
| `location` | string |  |
| `name` | string |  |
| `roles` | array<string> |  |
| `start_date` | string |  |
| `status` | string |  |
| `team_id` | string |  |
| `types` | array<string> |  |

## Native endpoint

Through the native EventGeek API, this operation is `GET /events/:event_id` (base URL `https://app.circa.co/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-event.md) for the provider-specific parameters and requirements.

