# Process Plan: List Active Automated Actions for Process Template Header



```
GET https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/list-active-automated-actions-for-process-template-header
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Process Plan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/list-active-automated-actions-for-process-template-header?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/list-active-automated-actions-for-process-template-header?${params}`, {
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
      "automated_action_list": [
        {
          "aa_acc_id": "string",
          "aa_action_type": 1,
          "aa_active": true,
          "aa_background": true,
          "aa_conditions_satisfied": 1,
          "aa_created_date_local": "2026-05-07T12:00:00.000Z",
          "aa_created_usr_id": "string",
          "aa_id": "string",
          "aa_integration_type": 1,
          "aa_modified_date_local": "2026-05-07T12:00:00.000Z",
          "aa_modified_usr_id": "string",
          "aa_name": "Ava Chen",
          "aa_repeat_minutes_unit_conversion": 1,
          "aa_repeat_minutes_unit_count": 1,
          "aa_th_id": "string",
          "aa_th_obj": {
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
            "th_name": "Ava Chen",
            "th_personal_task": true,
            "th_pg_id": "string",
            "th_prevent_delete": true,
            "th_primary_dt_publish": true,
            "th_priority": 1,
            "th_send_launch_response_email": true,
            "th_start_tr_id": "string"
          },
          "aa_trigger_day_num": 1,
          "aa_trigger_end_time": 1,
          "aa_trigger_friday": true,
          "aa_trigger_minutes_unit_conversion": 1,
          "aa_trigger_minutes_unit_count": 1,
          "aa_trigger_monday": true,
          "aa_trigger_month_num": 1,
          "aa_trigger_on_canceled": true,
          "aa_trigger_on_completed": true,
          "aa_trigger_saturday": true,
          "aa_trigger_schedule_type": 1,
          "aa_trigger_start_time": 1,
          "aa_trigger_sunday": true,
          "aa_trigger_thursday": true,
          "aa_trigger_tuesday": true,
          "aa_trigger_type": 1,
          "aa_trigger_wednesday": true,
          "aa_trigger_week_num": 1
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
| `automated_action_list[].aa_acc_id` | string |  |
| `automated_action_list[].aa_action_type` | number |  |
| `automated_action_list[].aa_active` | boolean |  |
| `automated_action_list[].aa_background` | boolean |  |
| `automated_action_list[].aa_conditions_satisfied` | number |  |
| `automated_action_list[].aa_created_date_local` | date |  |
| `automated_action_list[].aa_created_usr_id` | string |  |
| `automated_action_list[].aa_id` | string |  |
| `automated_action_list[].aa_integration_type` | number |  |
| `automated_action_list[].aa_modified_date_local` | date |  |
| `automated_action_list[].aa_modified_usr_id` | string |  |
| `automated_action_list[].aa_name` | string |  |
| `automated_action_list[].aa_repeat_minutes_unit_conversion` | number |  |
| `automated_action_list[].aa_repeat_minutes_unit_count` | number |  |
| `automated_action_list[].aa_th_id` | string |  |
| `automated_action_list[].aa_th_obj.th_acc_id` | string |  |
| `automated_action_list[].aa_th_obj.th_created_date_local` | date |  |
| `automated_action_list[].aa_th_obj.th_created_usr_id` | string |  |
| `automated_action_list[].aa_th_obj.th_deploy_version_changes` | boolean |  |
| `automated_action_list[].aa_th_obj.th_display_start` | boolean |  |
| `automated_action_list[].aa_th_obj.th_expire_public_instance_tokens` | boolean |  |
| `automated_action_list[].aa_th_obj.th_icon_name` | string |  |
| `automated_action_list[].aa_th_obj.th_id` | string |  |
| `automated_action_list[].aa_th_obj.th_instance_description_formula` | string |  |
| `automated_action_list[].aa_th_obj.th_launch_full_screen` | boolean |  |
| `automated_action_list[].aa_th_obj.th_median_duration_seconds` | number |  |
| `automated_action_list[].aa_th_obj.th_median_time_seconds` | number |  |
| `automated_action_list[].aa_th_obj.th_modified_date_local` | date |  |
| `automated_action_list[].aa_th_obj.th_modified_usr_id` | string |  |
| `automated_action_list[].aa_th_obj.th_name` | string |  |
| `automated_action_list[].aa_th_obj.th_personal_task` | boolean |  |
| `automated_action_list[].aa_th_obj.th_pg_id` | string |  |
| `automated_action_list[].aa_th_obj.th_prevent_delete` | boolean |  |
| `automated_action_list[].aa_th_obj.th_primary_dt_publish` | boolean |  |
| `automated_action_list[].aa_th_obj.th_priority` | number |  |
| `automated_action_list[].aa_th_obj.th_send_launch_response_email` | boolean |  |
| `automated_action_list[].aa_th_obj.th_start_tr_id` | string |  |
| `automated_action_list[].aa_trigger_day_num` | number |  |
| `automated_action_list[].aa_trigger_end_time` | number |  |
| `automated_action_list[].aa_trigger_friday` | boolean |  |
| `automated_action_list[].aa_trigger_minutes_unit_conversion` | number |  |
| `automated_action_list[].aa_trigger_minutes_unit_count` | number |  |
| `automated_action_list[].aa_trigger_monday` | boolean |  |
| `automated_action_list[].aa_trigger_month_num` | number |  |
| `automated_action_list[].aa_trigger_on_canceled` | boolean |  |
| `automated_action_list[].aa_trigger_on_completed` | boolean |  |
| `automated_action_list[].aa_trigger_saturday` | boolean |  |
| `automated_action_list[].aa_trigger_schedule_type` | number |  |
| `automated_action_list[].aa_trigger_start_time` | number |  |
| `automated_action_list[].aa_trigger_sunday` | boolean |  |
| `automated_action_list[].aa_trigger_thursday` | boolean |  |
| `automated_action_list[].aa_trigger_tuesday` | boolean |  |
| `automated_action_list[].aa_trigger_type` | number |  |
| `automated_action_list[].aa_trigger_wednesday` | boolean |  |
| `automated_action_list[].aa_trigger_week_num` | number |  |

## Native endpoint

Through the native Process Plan API, this operation is `GET /process_template_header/:processTemplateHeaderId/automated_action/list/active` (base URL `https://apius0.processplan.com/api/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-active-automated-actions-for-process-template-header.md) for the provider-specific parameters and requirements.

