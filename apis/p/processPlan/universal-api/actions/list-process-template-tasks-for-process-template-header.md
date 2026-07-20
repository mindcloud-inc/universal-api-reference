# Process Plan: List Process Template Tasks for Process Template Header



```
GET https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/list-process-template-tasks-for-process-template-header
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Process Plan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/list-process-template-tasks-for-process-template-header?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/list-process-template-tasks-for-process-template-header?${params}`, {
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
| `processTemplateHeaderId` | string | no | Process template header ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "process_template_task_list": [
        {
          "tt_acc_id": "string",
          "tt_allow_multiple_instances": true,
          "tt_allow_name_edit": true,
          "tt_allow_read_only_edit": true,
          "tt_allow_reassign": true,
          "tt_assignment_name": "Ava Chen",
          "tt_assignment_pic": "string",
          "tt_assignment_type": 1,
          "tt_checklist_requirement": 1,
          "tt_complete_all_pending_subprocesses_first": true,
          "tt_complete_all_pending_tasks_first": true,
          "tt_created_date_local": "2026-05-07T12:00:00.000Z",
          "tt_created_usr_id": "string",
          "tt_default_friday": true,
          "tt_default_monday": true,
          "tt_default_saturday": true,
          "tt_default_sunday": true,
          "tt_default_thursday": true,
          "tt_default_tuesday": true,
          "tt_default_wednesday": true,
          "tt_due_date_formula": "string",
          "tt_due_pivot_minutes": 1,
          "tt_due_pivot_minutes_unit_conversion": 1,
          "tt_due_pivot_minutes_unit_count": 1,
          "tt_editable_dates": true,
          "tt_estimated_duration_seconds": 1,
          "tt_hide_notes": true,
          "tt_id": "string",
          "tt_median_duration_seconds": 1,
          "tt_median_time_seconds": 1,
          "tt_mli_optimize": true,
          "tt_modified_date_local": "2026-05-07T12:00:00.000Z",
          "tt_modified_usr_id": "string",
          "tt_name": "Ava Chen",
          "tt_pivot_date_type": 1,
          "tt_public_task": true,
          "tt_send_assignment_emails": true,
          "tt_show_next_public_task": true,
          "tt_start_date_formula": "string",
          "tt_start_pivot_minutes": 1,
          "tt_start_pivot_minutes_unit_conversion": 1,
          "tt_start_pivot_minutes_unit_count": 1,
          "tt_tag_text": "string",
          "tt_tf_visibility_type": 1,
          "tt_th_id": "string",
          "tt_th_obj": {
            "th_icon_name": "Ava Chen",
            "th_id": "string",
            "th_name": "Ava Chen"
          },
          "tt_validate_preceding_paths": true
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
| `process_template_task_list[].tt_acc_id` | string |  |
| `process_template_task_list[].tt_allow_multiple_instances` | boolean |  |
| `process_template_task_list[].tt_allow_name_edit` | boolean |  |
| `process_template_task_list[].tt_allow_read_only_edit` | boolean |  |
| `process_template_task_list[].tt_allow_reassign` | boolean |  |
| `process_template_task_list[].tt_assignment_name` | string |  |
| `process_template_task_list[].tt_assignment_pic` | string |  |
| `process_template_task_list[].tt_assignment_type` | number |  |
| `process_template_task_list[].tt_checklist_requirement` | number |  |
| `process_template_task_list[].tt_complete_all_pending_subprocesses_first` | boolean |  |
| `process_template_task_list[].tt_complete_all_pending_tasks_first` | boolean |  |
| `process_template_task_list[].tt_created_date_local` | date |  |
| `process_template_task_list[].tt_created_usr_id` | string |  |
| `process_template_task_list[].tt_default_friday` | boolean |  |
| `process_template_task_list[].tt_default_monday` | boolean |  |
| `process_template_task_list[].tt_default_saturday` | boolean |  |
| `process_template_task_list[].tt_default_sunday` | boolean |  |
| `process_template_task_list[].tt_default_thursday` | boolean |  |
| `process_template_task_list[].tt_default_tuesday` | boolean |  |
| `process_template_task_list[].tt_default_wednesday` | boolean |  |
| `process_template_task_list[].tt_due_date_formula` | string |  |
| `process_template_task_list[].tt_due_pivot_minutes` | number |  |
| `process_template_task_list[].tt_due_pivot_minutes_unit_conversion` | number |  |
| `process_template_task_list[].tt_due_pivot_minutes_unit_count` | number |  |
| `process_template_task_list[].tt_editable_dates` | boolean |  |
| `process_template_task_list[].tt_estimated_duration_seconds` | number |  |
| `process_template_task_list[].tt_hide_notes` | boolean |  |
| `process_template_task_list[].tt_id` | string |  |
| `process_template_task_list[].tt_median_duration_seconds` | number |  |
| `process_template_task_list[].tt_median_time_seconds` | number |  |
| `process_template_task_list[].tt_mli_optimize` | boolean |  |
| `process_template_task_list[].tt_modified_date_local` | date |  |
| `process_template_task_list[].tt_modified_usr_id` | string |  |
| `process_template_task_list[].tt_name` | string |  |
| `process_template_task_list[].tt_pivot_date_type` | number |  |
| `process_template_task_list[].tt_public_task` | boolean |  |
| `process_template_task_list[].tt_send_assignment_emails` | boolean |  |
| `process_template_task_list[].tt_show_next_public_task` | boolean |  |
| `process_template_task_list[].tt_start_date_formula` | string |  |
| `process_template_task_list[].tt_start_pivot_minutes` | number |  |
| `process_template_task_list[].tt_start_pivot_minutes_unit_conversion` | number |  |
| `process_template_task_list[].tt_start_pivot_minutes_unit_count` | number |  |
| `process_template_task_list[].tt_tag_text` | string |  |
| `process_template_task_list[].tt_tf_visibility_type` | number |  |
| `process_template_task_list[].tt_th_id` | string |  |
| `process_template_task_list[].tt_th_obj.th_icon_name` | string |  |
| `process_template_task_list[].tt_th_obj.th_id` | string |  |
| `process_template_task_list[].tt_th_obj.th_name` | string |  |
| `process_template_task_list[].tt_validate_preceding_paths` | boolean |  |

## Native endpoint

Through the native Process Plan API, this operation is `GET /process_template_header/:processTemplateHeaderId/process_template_task/list` (base URL `https://apius0.processplan.com/api/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-process-template-tasks-for-process-template-header.md) for the provider-specific parameters and requirements.

