# Pipeline CRM: Retrieve Calendar Entry

Retrieves a calendar entry from Pipeline CRM.

```
GET https://connect.mindcloud.co/v1/universal/pipelineCRM/latest/actions/retrieve-calendar-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pipeline CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pipelineCRM/latest/actions/retrieve-calendar-entry?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pipelineCRM/latest/actions/retrieve-calendar-entry?${params}`, {
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
| `id` | number | yes | Calendar entry ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "all_day": true,
      "association_id": 1,
      "association_type": "string",
      "base_entry_id": 1,
      "calendar_entry_priority": {},
      "calendar_entry_priority_id": 1,
      "category": {},
      "category_id": 1,
      "company_id": 1,
      "complete": true,
      "completed_at": "string",
      "created_at": "string",
      "description": "string",
      "due_date": "2026-05-07T12:00:00.000Z",
      "end_time": "string",
      "exdate": "string",
      "exrule": "string",
      "google_calendar_id": "string",
      "id": 1,
      "name": "Ava Chen",
      "owner": {},
      "owner_id": 1,
      "part_of_recurring_series": true,
      "rdate": "string",
      "recurrence_end": "2026-05-07T12:00:00.000Z",
      "rrule": "string",
      "start_time": "string",
      "type": "string",
      "updated_at": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `all_day` | boolean |  |
| `association_id` | number |  |
| `association_type` | string |  |
| `base_entry_id` | number |  |
| `calendar_entry_priority` | object |  |
| `calendar_entry_priority_id` | number |  |
| `category` | object |  |
| `category_id` | number |  |
| `company_id` | number |  |
| `complete` | boolean |  |
| `completed_at` | string |  |
| `created_at` | string |  |
| `description` | string |  |
| `due_date` | date |  |
| `end_time` | string |  |
| `exdate` | string |  |
| `exrule` | string |  |
| `google_calendar_id` | string |  |
| `id` | number |  |
| `name` | string |  |
| `owner` | object |  |
| `owner_id` | number |  |
| `part_of_recurring_series` | boolean |  |
| `rdate` | string |  |
| `recurrence_end` | date |  |
| `rrule` | string |  |
| `start_time` | string |  |
| `type` | string |  |
| `updated_at` | string |  |

## Native endpoint

Through the native Pipeline CRM API, this operation is `GET /calendar_entries/:id` (base URL `https://api.pipelinecrm.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-calendar-entry.md) for the provider-specific parameters and requirements.

