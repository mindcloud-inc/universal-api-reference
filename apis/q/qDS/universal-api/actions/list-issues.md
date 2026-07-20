# QDS: List Issues



```
GET https://connect.mindcloud.co/v1/universal/qDS/latest/actions/list-issues
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QDS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/qDS/latest/actions/list-issues?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/qDS/latest/actions/list-issues?${params}`, {
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
      "issues": [
        {
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
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `issues[].client_id` | number |  |
| `issues[].client_name` | string |  |
| `issues[].complaint_id` | number |  |
| `issues[].complaint_name` | string |  |
| `issues[].cost` | number |  |
| `issues[].created_at` | date |  |
| `issues[].deleted_at` | date |  |
| `issues[].employee_id` | string |  |
| `issues[].employee_name` | string |  |
| `issues[].id` | number |  |
| `issues[].image_path` | string |  |
| `issues[].issue_date` | date |  |
| `issues[].office_notes` | string |  |
| `issues[].override` | boolean |  |
| `issues[].override_reason` | string |  |
| `issues[].previous_selected_warning_level` | number |  |
| `issues[].previous_selected_warning_type` | string |  |
| `issues[].role_id` | number |  |
| `issues[].survey_id` | string |  |
| `issues[].updated_at` | date |  |
| `issues[].user_id` | number |  |
| `issues[].user_name` | string |  |
| `issues[].warning_level` | number |  |
| `issues[].warning_type` | string |  |

## Native endpoint

Through the native QDS API, this operation is `GET /issues` (base URL `https://qdsapp.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-issues.md) for the provider-specific parameters and requirements.

