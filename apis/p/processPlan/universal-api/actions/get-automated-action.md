# Process Plan: Get Automated Action



```
GET https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/get-automated-action
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Process Plan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/get-automated-action?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/get-automated-action?${params}`, {
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
| `automatedActionId` | string | no | Automated action ID. |

## Response

```json
{
  "success": true,
  "data": [
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
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `aa_acc_id` | string |  |
| `aa_action_type` | number |  |
| `aa_active` | boolean |  |
| `aa_background` | boolean |  |
| `aa_conditions_satisfied` | number |  |
| `aa_created_date_local` | date |  |
| `aa_created_usr_id` | string |  |
| `aa_id` | string |  |
| `aa_integration_type` | number |  |
| `aa_modified_date_local` | date |  |
| `aa_modified_usr_id` | string |  |
| `aa_name` | string |  |
| `aa_repeat_minutes_unit_conversion` | number |  |
| `aa_repeat_minutes_unit_count` | number |  |
| `aa_th_id` | string |  |
| `aa_th_obj.th_acc_id` | string |  |
| `aa_th_obj.th_created_date_local` | date |  |
| `aa_th_obj.th_created_usr_id` | string |  |
| `aa_th_obj.th_deploy_version_changes` | boolean |  |
| `aa_th_obj.th_display_start` | boolean |  |
| `aa_th_obj.th_expire_public_instance_tokens` | boolean |  |
| `aa_th_obj.th_icon_name` | string |  |
| `aa_th_obj.th_id` | string |  |
| `aa_th_obj.th_instance_description_formula` | string |  |
| `aa_th_obj.th_launch_full_screen` | boolean |  |
| `aa_th_obj.th_median_duration_seconds` | number |  |
| `aa_th_obj.th_median_time_seconds` | number |  |
| `aa_th_obj.th_modified_date_local` | date |  |
| `aa_th_obj.th_modified_usr_id` | string |  |
| `aa_th_obj.th_name` | string |  |
| `aa_th_obj.th_personal_task` | boolean |  |
| `aa_th_obj.th_pg_id` | string |  |
| `aa_th_obj.th_prevent_delete` | boolean |  |
| `aa_th_obj.th_primary_dt_publish` | boolean |  |
| `aa_th_obj.th_priority` | number |  |
| `aa_th_obj.th_send_launch_response_email` | boolean |  |
| `aa_th_obj.th_start_tr_id` | string |  |
| `aa_trigger_day_num` | number |  |
| `aa_trigger_end_time` | number |  |
| `aa_trigger_friday` | boolean |  |
| `aa_trigger_minutes_unit_conversion` | number |  |
| `aa_trigger_minutes_unit_count` | number |  |
| `aa_trigger_monday` | boolean |  |
| `aa_trigger_month_num` | number |  |
| `aa_trigger_on_canceled` | boolean |  |
| `aa_trigger_on_completed` | boolean |  |
| `aa_trigger_saturday` | boolean |  |
| `aa_trigger_schedule_type` | number |  |
| `aa_trigger_start_time` | number |  |
| `aa_trigger_sunday` | boolean |  |
| `aa_trigger_thursday` | boolean |  |
| `aa_trigger_tuesday` | boolean |  |
| `aa_trigger_type` | number |  |
| `aa_trigger_wednesday` | boolean |  |
| `aa_trigger_week_num` | number |  |

## Native endpoint

Through the native Process Plan API, this operation is `GET /automated_action/:automatedActionId` (base URL `https://apius0.processplan.com/api/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-automated-action.md) for the provider-specific parameters and requirements.

