# Process Plan: List Pending Process Instance Tasks for User Group



```
GET https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/list-pending-process-instance-tasks-for-user-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Process Plan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/list-pending-process-instance-tasks-for-user-group?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/list-pending-process-instance-tasks-for-user-group?${params}`, {
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
      "process_instance_task_list": [
        {
          "it_acc_id": "string",
          "it_actual_time_seconds": 1,
          "it_assigned_date_local": "2026-05-07T12:00:00.000Z",
          "it_assigned_name": "Ava Chen",
          "it_assigned_ug_id": "string",
          "it_assigned_ug_obj": {
            "ug_id": "string",
            "ug_name": "Ava Chen"
          },
          "it_assigned_usr_id": "string",
          "it_assigned_usr_obj": {
            "usr_email_address": "ava@example.com",
            "usr_first_name": "Ava",
            "usr_full_name": "Ava Chen",
            "usr_id": "string",
            "usr_last_name": "Chen",
            "usr_profile_pic_url": "https://example.com"
          },
          "it_created_date_local": "2026-05-07T12:00:00.000Z",
          "it_created_usr_id": "string",
          "it_due_today": true,
          "it_id": "string",
          "it_ih_id": "string",
          "it_ih_obj": {
            "ih_created_date_local": "2026-05-07T12:00:00.000Z",
            "ih_id": "string",
            "ih_instance_description": "string",
            "ih_personal_task": true,
            "ih_progress_percentage": 1,
            "ih_test_mode": true,
            "ih_th_id": "string"
          },
          "it_instance_description": "string",
          "it_modified_date_local": "2026-05-07T12:00:00.000Z",
          "it_modified_usr_id": "string",
          "it_name": "Ava Chen",
          "it_notes": "string",
          "it_past_due": true,
          "it_tag_text": "string",
          "it_th_id": "string",
          "it_th_obj": {
            "th_icon_name": "Ava Chen",
            "th_id": "string",
            "th_name": "Ava Chen",
            "th_pg_obj": {
              "pg_icon_name": "Ava Chen",
              "pg_id": "string",
              "pg_name": "Ava Chen"
            }
          },
          "it_tt_id": "string",
          "it_tt_obj": {
            "tt_allow_name_edit": true,
            "tt_checklist_requirement": 1,
            "tt_editable_dates": true,
            "tt_hide_notes": true,
            "tt_id": "string",
            "tt_instructions": "string",
            "tt_name": "Ava Chen",
            "tt_tag_text": "string",
            "tt_tf_visibility_type": 1
          }
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
| `process_instance_task_list[].it_acc_id` | string |  |
| `process_instance_task_list[].it_actual_time_seconds` | number |  |
| `process_instance_task_list[].it_assigned_date_local` | date |  |
| `process_instance_task_list[].it_assigned_name` | string |  |
| `process_instance_task_list[].it_assigned_ug_id` | string |  |
| `process_instance_task_list[].it_assigned_ug_obj.ug_id` | string |  |
| `process_instance_task_list[].it_assigned_ug_obj.ug_name` | string |  |
| `process_instance_task_list[].it_assigned_usr_id` | string |  |
| `process_instance_task_list[].it_assigned_usr_obj.usr_email_address` | string |  |
| `process_instance_task_list[].it_assigned_usr_obj.usr_first_name` | string |  |
| `process_instance_task_list[].it_assigned_usr_obj.usr_full_name` | string |  |
| `process_instance_task_list[].it_assigned_usr_obj.usr_id` | string |  |
| `process_instance_task_list[].it_assigned_usr_obj.usr_last_name` | string |  |
| `process_instance_task_list[].it_assigned_usr_obj.usr_profile_pic_url` | string |  |
| `process_instance_task_list[].it_created_date_local` | date |  |
| `process_instance_task_list[].it_created_usr_id` | string |  |
| `process_instance_task_list[].it_due_today` | boolean |  |
| `process_instance_task_list[].it_id` | string |  |
| `process_instance_task_list[].it_ih_id` | string |  |
| `process_instance_task_list[].it_ih_obj.ih_created_date_local` | date |  |
| `process_instance_task_list[].it_ih_obj.ih_id` | string |  |
| `process_instance_task_list[].it_ih_obj.ih_instance_description` | string |  |
| `process_instance_task_list[].it_ih_obj.ih_personal_task` | boolean |  |
| `process_instance_task_list[].it_ih_obj.ih_progress_percentage` | number |  |
| `process_instance_task_list[].it_ih_obj.ih_test_mode` | boolean |  |
| `process_instance_task_list[].it_ih_obj.ih_th_id` | string |  |
| `process_instance_task_list[].it_instance_description` | string |  |
| `process_instance_task_list[].it_modified_date_local` | date |  |
| `process_instance_task_list[].it_modified_usr_id` | string |  |
| `process_instance_task_list[].it_name` | string |  |
| `process_instance_task_list[].it_notes` | string |  |
| `process_instance_task_list[].it_past_due` | boolean |  |
| `process_instance_task_list[].it_tag_text` | string |  |
| `process_instance_task_list[].it_th_id` | string |  |
| `process_instance_task_list[].it_th_obj.th_icon_name` | string |  |
| `process_instance_task_list[].it_th_obj.th_id` | string |  |
| `process_instance_task_list[].it_th_obj.th_name` | string |  |
| `process_instance_task_list[].it_th_obj.th_pg_obj.pg_icon_name` | string |  |
| `process_instance_task_list[].it_th_obj.th_pg_obj.pg_id` | string |  |
| `process_instance_task_list[].it_th_obj.th_pg_obj.pg_name` | string |  |
| `process_instance_task_list[].it_tt_id` | string |  |
| `process_instance_task_list[].it_tt_obj.tt_allow_name_edit` | boolean |  |
| `process_instance_task_list[].it_tt_obj.tt_checklist_requirement` | number |  |
| `process_instance_task_list[].it_tt_obj.tt_editable_dates` | boolean |  |
| `process_instance_task_list[].it_tt_obj.tt_hide_notes` | boolean |  |
| `process_instance_task_list[].it_tt_obj.tt_id` | string |  |
| `process_instance_task_list[].it_tt_obj.tt_instructions` | string |  |
| `process_instance_task_list[].it_tt_obj.tt_name` | string |  |
| `process_instance_task_list[].it_tt_obj.tt_tag_text` | string |  |
| `process_instance_task_list[].it_tt_obj.tt_tf_visibility_type` | number |  |

## Native endpoint

Through the native Process Plan API, this operation is `GET /user_group/:userGroupId/process_instance_task/list/pending` (base URL `https://apius0.processplan.com/api/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-pending-process-instance-tasks-for-user-group.md) for the provider-specific parameters and requirements.

