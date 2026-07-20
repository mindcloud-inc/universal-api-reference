# Process Plan: Get User Group



```
GET https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/get-user-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Process Plan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/get-user-group?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/get-user-group?${params}`, {
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
| `userGroupId` | string | no | User group ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ug_ac_batch_processing": true,
      "ug_ac_cancel_processes": true,
      "ug_ac_change_task_assignments": true,
      "ug_ac_create_process_templates": true,
      "ug_ac_edit_account_information": true,
      "ug_ac_edit_instance_diagrams": true,
      "ug_ac_edit_process_templates": true,
      "ug_ac_edit_subscription": true,
      "ug_ac_edit_users": true,
      "ug_ac_launch_processes": true,
      "ug_ac_restart_instance_tasks": true,
      "ug_ac_use_ai": true,
      "ug_ac_view_process_reports": true,
      "ug_acc_id": "string",
      "ug_created_date_local": "2026-05-07T12:00:00.000Z",
      "ug_created_usr_id": "string",
      "ug_icon_name": "Ava Chen",
      "ug_id": "string",
      "ug_modified_date_local": "2026-05-07T12:00:00.000Z",
      "ug_modified_usr_id": "string",
      "ug_name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ug_ac_batch_processing` | boolean |  |
| `ug_ac_cancel_processes` | boolean |  |
| `ug_ac_change_task_assignments` | boolean |  |
| `ug_ac_create_process_templates` | boolean |  |
| `ug_ac_edit_account_information` | boolean |  |
| `ug_ac_edit_instance_diagrams` | boolean |  |
| `ug_ac_edit_process_templates` | boolean |  |
| `ug_ac_edit_subscription` | boolean |  |
| `ug_ac_edit_users` | boolean |  |
| `ug_ac_launch_processes` | boolean |  |
| `ug_ac_restart_instance_tasks` | boolean |  |
| `ug_ac_use_ai` | boolean |  |
| `ug_ac_view_process_reports` | boolean |  |
| `ug_acc_id` | string |  |
| `ug_created_date_local` | date |  |
| `ug_created_usr_id` | string |  |
| `ug_icon_name` | string |  |
| `ug_id` | string |  |
| `ug_modified_date_local` | date |  |
| `ug_modified_usr_id` | string |  |
| `ug_name` | string |  |

## Native endpoint

Through the native Process Plan API, this operation is `GET /user_group/:userGroupId` (base URL `https://apius0.processplan.com/api/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-group.md) for the provider-specific parameters and requirements.

