# Process Plan: Get AI Agent Job for Process Template Task



```
GET https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/get-ai-agent-job-for-process-template-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Process Plan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/get-ai-agent-job-for-process-template-task?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/get-ai-agent-job-for-process-template-task?${params}`, {
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
| `processTemplateTaskId` | string | no | Process template task ID. |

## Response

```json
{
  "success": true,
  "data": [
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
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `tt_acc_id` | string |  |
| `tt_allow_multiple_instances` | boolean |  |
| `tt_allow_name_edit` | boolean |  |
| `tt_allow_read_only_edit` | boolean |  |
| `tt_allow_reassign` | boolean |  |
| `tt_assignment_name` | string |  |
| `tt_assignment_pic` | string |  |
| `tt_assignment_type` | number |  |
| `tt_checklist_requirement` | number |  |
| `tt_complete_all_pending_subprocesses_first` | boolean |  |
| `tt_complete_all_pending_tasks_first` | boolean |  |
| `tt_created_date_local` | date |  |
| `tt_created_usr_id` | string |  |
| `tt_default_friday` | boolean |  |
| `tt_default_monday` | boolean |  |
| `tt_default_saturday` | boolean |  |
| `tt_default_sunday` | boolean |  |
| `tt_default_thursday` | boolean |  |
| `tt_default_tuesday` | boolean |  |
| `tt_default_wednesday` | boolean |  |
| `tt_due_date_formula` | string |  |
| `tt_due_pivot_minutes` | number |  |
| `tt_due_pivot_minutes_unit_conversion` | number |  |
| `tt_due_pivot_minutes_unit_count` | number |  |
| `tt_editable_dates` | boolean |  |
| `tt_estimated_duration_seconds` | number |  |
| `tt_hide_notes` | boolean |  |
| `tt_id` | string |  |
| `tt_median_duration_seconds` | number |  |
| `tt_median_time_seconds` | number |  |
| `tt_mli_optimize` | boolean |  |
| `tt_modified_date_local` | date |  |
| `tt_modified_usr_id` | string |  |
| `tt_name` | string |  |
| `tt_pivot_date_type` | number |  |
| `tt_public_task` | boolean |  |
| `tt_send_assignment_emails` | boolean |  |
| `tt_show_next_public_task` | boolean |  |
| `tt_start_date_formula` | string |  |
| `tt_start_pivot_minutes` | number |  |
| `tt_start_pivot_minutes_unit_conversion` | number |  |
| `tt_start_pivot_minutes_unit_count` | number |  |
| `tt_tag_text` | string |  |
| `tt_tf_visibility_type` | number |  |
| `tt_th_id` | string |  |
| `tt_th_obj.th_icon_name` | string |  |
| `tt_th_obj.th_id` | string |  |
| `tt_th_obj.th_name` | string |  |
| `tt_validate_preceding_paths` | boolean |  |

## Native endpoint

Through the native Process Plan API, this operation is `GET /process_template_task/:processTemplateTaskId/ai_agent_job` (base URL `https://apius0.processplan.com/api/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-ai-agent-job-for-process-template-task.md) for the provider-specific parameters and requirements.

