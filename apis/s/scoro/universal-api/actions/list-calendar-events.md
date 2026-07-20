# Scoro: List Calendar Events

Retrieves calendar events from Scoro.

```
GET https://connect.mindcloud.co/v1/universal/scoro/latest/actions/list-calendar-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scoro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scoro/latest/actions/list-calendar-events?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scoro/latest/actions/list-calendar-events?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "activity_id": 1,
      "activity_type": "string",
      "call_link": "https://example.com",
      "company_id": 1,
      "created_date": "string",
      "description": "string",
      "duration_planned": "string",
      "end_datetime": "string",
      "event_id": 1,
      "event_name": "Ava Chen",
      "event_type": "string",
      "full_day_event": 1,
      "guests": [
        {}
      ],
      "modified_date": "string",
      "owner_email": "ava@example.com",
      "owner_id": 1,
      "person_id": 1,
      "project_id": 1,
      "project_name": "Ava Chen",
      "repeat_id": 1,
      "start_datetime": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activity_id` | number |  |
| `activity_type` | string |  |
| `call_link` | string |  |
| `company_id` | number |  |
| `created_date` | string |  |
| `description` | string |  |
| `duration_planned` | string |  |
| `end_datetime` | string |  |
| `event_id` | number |  |
| `event_name` | string |  |
| `event_type` | string |  |
| `full_day_event` | number |  |
| `guests` | array<object> |  |
| `modified_date` | string |  |
| `owner_email` | string |  |
| `owner_id` | number |  |
| `person_id` | number |  |
| `project_id` | number |  |
| `project_name` | string |  |
| `repeat_id` | number |  |
| `start_datetime` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Scoro API, this operation is `POST calendar/list` (base URL `{{credentials.subdomain}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-calendar-events.md) for the provider-specific parameters and requirements.

