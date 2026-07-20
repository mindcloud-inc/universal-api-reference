# QDS: Get Issue



```
GET https://connect.mindcloud.co/v1/universal/qDS/latest/actions/get-issue
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QDS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/qDS/latest/actions/get-issue?connectionId=$CONNECTION_ID&issueId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "issueId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/qDS/latest/actions/get-issue?${params}`, {
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
| `issueId` | number | yes | The QDS issue ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "issue": {
        "client_id": 1,
        "client_name": "Ava Chen",
        "complaint_id": 1,
        "complaint_name": "Ava Chen",
        "cost": 1,
        "created_at": "2026-05-07T12:00:00.000Z",
        "deleted_at": "2026-05-07T12:00:00.000Z",
        "employee_id": "string",
        "employee_name": "Ava Chen",
        "id": 1,
        "image_path": "string",
        "issue_date": "2026-05-07T12:00:00.000Z",
        "office_notes": "string",
        "override": true,
        "override_reason": "string",
        "previous_selected_warning_level": 1,
        "previous_selected_warning_type": "string",
        "role_id": 1,
        "survey_id": "string",
        "updated_at": "2026-05-07T12:00:00.000Z",
        "user_id": 1,
        "user_name": "Ava Chen",
        "warning_level": 1,
        "warning_type": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `issue.client_id` | number |  |
| `issue.client_name` | string |  |
| `issue.complaint_id` | number |  |
| `issue.complaint_name` | string |  |
| `issue.cost` | number |  |
| `issue.created_at` | date |  |
| `issue.deleted_at` | date |  |
| `issue.employee_id` | string |  |
| `issue.employee_name` | string |  |
| `issue.id` | number |  |
| `issue.image_path` | string |  |
| `issue.issue_date` | date |  |
| `issue.office_notes` | string |  |
| `issue.override` | boolean |  |
| `issue.override_reason` | string |  |
| `issue.previous_selected_warning_level` | number |  |
| `issue.previous_selected_warning_type` | string |  |
| `issue.role_id` | number |  |
| `issue.survey_id` | string |  |
| `issue.updated_at` | date |  |
| `issue.user_id` | number |  |
| `issue.user_name` | string |  |
| `issue.warning_level` | number |  |
| `issue.warning_type` | string |  |

## Native endpoint

Through the native QDS API, this operation is `GET /issues/:issueId` (base URL `https://qdsapp.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-issue.md) for the provider-specific parameters and requirements.

