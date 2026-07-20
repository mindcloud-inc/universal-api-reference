# Cerbo: List Tasks

Retrieves task records from Cerbo.

```
GET https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/list-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cerbo `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/list-tasks?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/list-tasks?${params}`, {
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
      "addedby": 1,
      "associated_resource_id": 1,
      "associated_resource_type": "string",
      "completed_on": "2026-05-07T12:00:00.000Z",
      "created": "2026-05-07T12:00:00.000Z",
      "dr_id": 1,
      "due_date": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "notes": "string",
      "object": "string",
      "patient_details": {
        "dob": "2026-05-07T12:00:00.000Z",
        "email1": "ava@example.com",
        "first_name": "Ava",
        "id": "string",
        "last_name": "Chen",
        "object": "string",
        "sex": "string",
        "url_patient_details": "https://example.com"
      },
      "priority": "string",
      "reminder_time": "2026-05-07T12:00:00.000Z",
      "start_date": "2026-05-07T12:00:00.000Z",
      "subject": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addedby` | number |  |
| `associated_resource_id` | number |  |
| `associated_resource_type` | string |  |
| `completed_on` | date |  |
| `created` | date |  |
| `dr_id` | number |  |
| `due_date` | date |  |
| `id` | number |  |
| `notes` | string |  |
| `object` | string |  |
| `patient_details` | object |  |
| `patient_details.dob` | date |  |
| `patient_details.email1` | string |  |
| `patient_details.first_name` | string |  |
| `patient_details.id` | string |  |
| `patient_details.last_name` | string |  |
| `patient_details.object` | string |  |
| `patient_details.sex` | string |  |
| `patient_details.url_patient_details` | string |  |
| `priority` | string |  |
| `reminder_time` | date |  |
| `start_date` | date |  |
| `subject` | string |  |

## Native endpoint

Through the native Cerbo API, this operation is `GET /task` (base URL `https://{{credentials.tenant}}.md-hq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-tasks.md) for the provider-specific parameters and requirements.

