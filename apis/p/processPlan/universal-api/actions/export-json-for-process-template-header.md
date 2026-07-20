# Process Plan: Export JSON for Process Template Header



```
GET https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/export-json-for-process-template-header
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Process Plan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/export-json-for-process-template-header?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/export-json-for-process-template-header?${params}`, {
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
      "process_template_field_list": [
        {
          "tf_acc_id": "string",
          "tf_calculate_type": 1,
          "tf_created_date_local": "2026-05-07T12:00:00.000Z",
          "tf_created_usr_id": "string",
          "tf_display_at_start": true,
          "tf_fl_analysis_type": 1,
          "tf_format_type": 1,
          "tf_id": "string",
          "tf_modified_date_local": "2026-05-07T12:00:00.000Z",
          "tf_modified_usr_id": "string",
          "tf_name": "Ava Chen",
          "tf_public_read_only": true,
          "tf_read_only": true,
          "tf_required": true,
          "tf_required_on_x": true,
          "tf_secure": true,
          "tf_share_with_parent": true,
          "tf_sort_num": 1,
          "tf_th_id": "string",
          "tf_type": 1,
          "tf_unique": true
        }
      ],
      "process_template_header_obj": {
        "th_acc_id": "string",
        "th_created_date_local": "2026-05-07T12:00:00.000Z",
        "th_created_usr_id": "string",
        "th_deploy_version_changes": true,
        "th_display_start": true,
        "th_expire_public_instance_tokens": true,
        "th_icon_name": "Ava Chen",
        "th_id": "string",
        "th_instance_description_formula": "string",
        "th_launch_full_screen": true,
        "th_median_duration_seconds": 1,
        "th_median_time_seconds": 1,
        "th_modified_date_local": "2026-05-07T12:00:00.000Z",
        "th_modified_usr_id": "string",
        "th_modified_usr_obj": {
          "usr_email_address": "ava@example.com",
          "usr_first_name": "Ava",
          "usr_full_name": "Ava Chen",
          "usr_id": "string",
          "usr_last_name": "Chen",
          "usr_profile_pic_url": "https://example.com"
        },
        "th_name": "Ava Chen",
        "th_personal_task": true,
        "th_pg_id": "string",
        "th_pg_obj": {
          "pg_icon_name": "Ava Chen",
          "pg_id": "string",
          "pg_name": "Ava Chen"
        },
        "th_prevent_delete": true,
        "th_primary_dt_publish": true,
        "th_priority": 1,
        "th_send_launch_response_email": true,
        "th_start_tr_id": "string"
      },
      "process_template_response_list": [
        {
          "tr_acc_id": "string",
          "tr_block_task_reassignment": true,
          "tr_bypass_required_fields": true,
          "tr_cancel_instance": true,
          "tr_created_date_local": "2026-05-07T12:00:00.000Z",
          "tr_created_usr_id": "string",
          "tr_exit_subprocess": true,
          "tr_favorable_rating": 1,
          "tr_frequency": 1,
          "tr_hide_if_past_due": true,
          "tr_id": "string",
          "tr_linked_from_tt_id": "https://example.com",
          "tr_max_selections": 1,
          "tr_modified_date_local": "2026-05-07T12:00:00.000Z",
          "tr_modified_usr_id": "string",
          "tr_name": "Ava Chen",
          "tr_next_task_delay_seconds": 1,
          "tr_note_required": true,
          "tr_process_in_background": true,
          "tr_sort_num": 1,
          "tr_universal_response": true
        }
      ],
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
          "tt_inbound_link_count": 1,
          "tt_linked_from_tr_id": "https://example.com",
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
| `process_template_field_list[].tf_acc_id` | string |  |
| `process_template_field_list[].tf_calculate_type` | number |  |
| `process_template_field_list[].tf_created_date_local` | date |  |
| `process_template_field_list[].tf_created_usr_id` | string |  |
| `process_template_field_list[].tf_display_at_start` | boolean |  |
| `process_template_field_list[].tf_fl_analysis_type` | number |  |
| `process_template_field_list[].tf_format_type` | number |  |
| `process_template_field_list[].tf_id` | string |  |
| `process_template_field_list[].tf_modified_date_local` | date |  |
| `process_template_field_list[].tf_modified_usr_id` | string |  |
| `process_template_field_list[].tf_name` | string |  |
| `process_template_field_list[].tf_public_read_only` | boolean |  |
| `process_template_field_list[].tf_read_only` | boolean |  |
| `process_template_field_list[].tf_required` | boolean |  |
| `process_template_field_list[].tf_required_on_x` | boolean |  |
| `process_template_field_list[].tf_secure` | boolean |  |
| `process_template_field_list[].tf_share_with_parent` | boolean |  |
| `process_template_field_list[].tf_sort_num` | number |  |
| `process_template_field_list[].tf_th_id` | string |  |
| `process_template_field_list[].tf_type` | number |  |
| `process_template_field_list[].tf_unique` | boolean |  |
| `process_template_header_obj.th_acc_id` | string |  |
| `process_template_header_obj.th_created_date_local` | date |  |
| `process_template_header_obj.th_created_usr_id` | string |  |
| `process_template_header_obj.th_deploy_version_changes` | boolean |  |
| `process_template_header_obj.th_display_start` | boolean |  |
| `process_template_header_obj.th_expire_public_instance_tokens` | boolean |  |
| `process_template_header_obj.th_icon_name` | string |  |
| `process_template_header_obj.th_id` | string |  |
| `process_template_header_obj.th_instance_description_formula` | string |  |
| `process_template_header_obj.th_launch_full_screen` | boolean |  |
| `process_template_header_obj.th_median_duration_seconds` | number |  |
| `process_template_header_obj.th_median_time_seconds` | number |  |
| `process_template_header_obj.th_modified_date_local` | date |  |
| `process_template_header_obj.th_modified_usr_id` | string |  |
| `process_template_header_obj.th_modified_usr_obj.usr_email_address` | string |  |
| `process_template_header_obj.th_modified_usr_obj.usr_first_name` | string |  |
| `process_template_header_obj.th_modified_usr_obj.usr_full_name` | string |  |
| `process_template_header_obj.th_modified_usr_obj.usr_id` | string |  |
| `process_template_header_obj.th_modified_usr_obj.usr_last_name` | string |  |
| `process_template_header_obj.th_modified_usr_obj.usr_profile_pic_url` | string |  |
| `process_template_header_obj.th_name` | string |  |
| `process_template_header_obj.th_personal_task` | boolean |  |
| `process_template_header_obj.th_pg_id` | string |  |
| `process_template_header_obj.th_pg_obj.pg_icon_name` | string |  |
| `process_template_header_obj.th_pg_obj.pg_id` | string |  |
| `process_template_header_obj.th_pg_obj.pg_name` | string |  |
| `process_template_header_obj.th_prevent_delete` | boolean |  |
| `process_template_header_obj.th_primary_dt_publish` | boolean |  |
| `process_template_header_obj.th_priority` | number |  |
| `process_template_header_obj.th_send_launch_response_email` | boolean |  |
| `process_template_header_obj.th_start_tr_id` | string |  |
| `process_template_response_list[].tr_acc_id` | string |  |
| `process_template_response_list[].tr_block_task_reassignment` | boolean |  |
| `process_template_response_list[].tr_bypass_required_fields` | boolean |  |
| `process_template_response_list[].tr_cancel_instance` | boolean |  |
| `process_template_response_list[].tr_created_date_local` | date |  |
| `process_template_response_list[].tr_created_usr_id` | string |  |
| `process_template_response_list[].tr_exit_subprocess` | boolean |  |
| `process_template_response_list[].tr_favorable_rating` | number |  |
| `process_template_response_list[].tr_frequency` | number |  |
| `process_template_response_list[].tr_hide_if_past_due` | boolean |  |
| `process_template_response_list[].tr_id` | string |  |
| `process_template_response_list[].tr_linked_from_tt_id` | string |  |
| `process_template_response_list[].tr_max_selections` | number |  |
| `process_template_response_list[].tr_modified_date_local` | date |  |
| `process_template_response_list[].tr_modified_usr_id` | string |  |
| `process_template_response_list[].tr_name` | string |  |
| `process_template_response_list[].tr_next_task_delay_seconds` | number |  |
| `process_template_response_list[].tr_note_required` | boolean |  |
| `process_template_response_list[].tr_process_in_background` | boolean |  |
| `process_template_response_list[].tr_sort_num` | number |  |
| `process_template_response_list[].tr_universal_response` | boolean |  |
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
| `process_template_task_list[].tt_inbound_link_count` | number |  |
| `process_template_task_list[].tt_linked_from_tr_id` | string |  |
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
| `process_template_task_list[].tt_validate_preceding_paths` | boolean |  |

## Native endpoint

Through the native Process Plan API, this operation is `GET /process_template_header/:processTemplateHeaderId/json_export` (base URL `https://apius0.processplan.com/api/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/export-json-for-process-template-header.md) for the provider-specific parameters and requirements.

