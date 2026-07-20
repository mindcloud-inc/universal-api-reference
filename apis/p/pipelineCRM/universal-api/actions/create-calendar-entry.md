# Pipeline CRM: Create Calendar Entry

Creates a new calendar task or event in Pipeline CRM.

```
POST https://connect.mindcloud.co/v1/universal/pipelineCRM/latest/actions/create-calendar-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pipeline CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pipelineCRM/latest/actions/create-calendar-entry" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "calendarEntry.categoryId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pipelineCRM/latest/actions/create-calendar-entry', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "calendarEntry.categoryId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `deliverAssignmentEmail` | boolean | no | Send an assignment email when the calendar entry is assigned to another user. Default: `true`. |
| `calendarEntry.type` | string | no | Calendar entry type: CalendarEvent or CalendarTask. |
| `calendarEntry.categoryId` | number | yes | The event category ID. |
| `calendarEntry.name` | string | no | The name of the task or event. |
| `calendarEntry.description` | string | no | A detailed description of the event. |
| `calendarEntry.startTime` | string | no | Start time for CalendarEvent entries. |
| `calendarEntry.endTime` | string | no | End time for CalendarEvent entries. |
| `calendarEntry.allDay` | boolean | no | Whether the event is all day. |
| `calendarEntry.dueDate` | date | no | Due date for CalendarTask entries. |
| `calendarEntry.complete` | boolean | no | Whether the entry is complete. |
| `calendarEntry.associationId` | number | no | The associated person, company, or deal ID. |
| `calendarEntry.associationType` | string | no | Association type: Deal, Company, or Person. |
| `calendarEntry.companyId` | number | no | If directly tied to a company, the company ID. |
| `calendarEntry.calendarEntryPriorityId` | number | no | The event priority ID. |

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

Through the native Pipeline CRM API, this operation is `POST /calendar_entries` (base URL `https://api.pipelinecrm.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-calendar-entry.md) for the provider-specific parameters and requirements.

