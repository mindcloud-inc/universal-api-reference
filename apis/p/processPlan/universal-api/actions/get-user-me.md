# Process Plan: Get User Me



```
GET https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/get-user-me
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Process Plan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/get-user-me?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/get-user-me?${params}`, {
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
      "account_obj": {
        "acc_allow_proxy_management": true,
        "acc_auto_submit_email_responses": true,
        "acc_billing_country_code": "string",
        "acc_created_date_local": "2026-05-07T12:00:00.000Z",
        "acc_date_format": 1,
        "acc_id": "string",
        "acc_name": "Ava Chen",
        "acc_public_user_ug_id": "string",
        "acc_robot_ug_id": "string",
        "acc_status": "string",
        "acc_ui_bar_color": "string"
      },
      "user_obj": {
        "usr_24_hour_time": true,
        "usr_acc_id": "string",
        "usr_assignment_emails": true,
        "usr_created_date_local": "2026-05-07T12:00:00.000Z",
        "usr_created_usr_id": "string",
        "usr_date_format": 1,
        "usr_email_address": "ava@example.com",
        "usr_first_name": "Ava",
        "usr_full_name": "Ava Chen",
        "usr_fullscreen_tasks": true,
        "usr_id": "string",
        "usr_language": "string",
        "usr_last_activity_date_local": "2026-05-07T12:00:00.000Z",
        "usr_last_name": "Chen",
        "usr_message_emails": true,
        "usr_modified_date_local": "2026-05-07T12:00:00.000Z",
        "usr_modified_usr_id": "string",
        "usr_permissions_ug_obj": {
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
          "ug_ac_view_all_templates": true,
          "ug_ac_view_process_reports": true
        },
        "usr_profile_pic_url": "https://example.com",
        "usr_require_mfa": true,
        "usr_ug_id_list": [
          "string"
        ],
        "usr_ug_name_list": [
          "Ava Chen"
        ],
        "usr_utc_offset": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account_obj.acc_allow_proxy_management` | boolean |  |
| `account_obj.acc_auto_submit_email_responses` | boolean |  |
| `account_obj.acc_billing_country_code` | string |  |
| `account_obj.acc_created_date_local` | date |  |
| `account_obj.acc_date_format` | number |  |
| `account_obj.acc_id` | string |  |
| `account_obj.acc_name` | string |  |
| `account_obj.acc_public_user_ug_id` | string |  |
| `account_obj.acc_robot_ug_id` | string |  |
| `account_obj.acc_status` | string |  |
| `account_obj.acc_ui_bar_color` | string |  |
| `user_obj.usr_24_hour_time` | boolean |  |
| `user_obj.usr_acc_id` | string |  |
| `user_obj.usr_assignment_emails` | boolean |  |
| `user_obj.usr_created_date_local` | date |  |
| `user_obj.usr_created_usr_id` | string |  |
| `user_obj.usr_date_format` | number |  |
| `user_obj.usr_email_address` | string |  |
| `user_obj.usr_first_name` | string |  |
| `user_obj.usr_full_name` | string |  |
| `user_obj.usr_fullscreen_tasks` | boolean |  |
| `user_obj.usr_id` | string |  |
| `user_obj.usr_language` | string |  |
| `user_obj.usr_last_activity_date_local` | date |  |
| `user_obj.usr_last_name` | string |  |
| `user_obj.usr_message_emails` | boolean |  |
| `user_obj.usr_modified_date_local` | date |  |
| `user_obj.usr_modified_usr_id` | string |  |
| `user_obj.usr_permissions_ug_obj.ug_ac_batch_processing` | boolean |  |
| `user_obj.usr_permissions_ug_obj.ug_ac_cancel_processes` | boolean |  |
| `user_obj.usr_permissions_ug_obj.ug_ac_change_task_assignments` | boolean |  |
| `user_obj.usr_permissions_ug_obj.ug_ac_create_process_templates` | boolean |  |
| `user_obj.usr_permissions_ug_obj.ug_ac_edit_account_information` | boolean |  |
| `user_obj.usr_permissions_ug_obj.ug_ac_edit_instance_diagrams` | boolean |  |
| `user_obj.usr_permissions_ug_obj.ug_ac_edit_process_templates` | boolean |  |
| `user_obj.usr_permissions_ug_obj.ug_ac_edit_subscription` | boolean |  |
| `user_obj.usr_permissions_ug_obj.ug_ac_edit_users` | boolean |  |
| `user_obj.usr_permissions_ug_obj.ug_ac_launch_processes` | boolean |  |
| `user_obj.usr_permissions_ug_obj.ug_ac_restart_instance_tasks` | boolean |  |
| `user_obj.usr_permissions_ug_obj.ug_ac_use_ai` | boolean |  |
| `user_obj.usr_permissions_ug_obj.ug_ac_view_all_templates` | boolean |  |
| `user_obj.usr_permissions_ug_obj.ug_ac_view_process_reports` | boolean |  |
| `user_obj.usr_profile_pic_url` | string |  |
| `user_obj.usr_require_mfa` | boolean |  |
| `user_obj.usr_ug_id_list[]` | string |  |
| `user_obj.usr_ug_name_list[]` | string |  |
| `user_obj.usr_utc_offset` | number |  |

## Native endpoint

Through the native Process Plan API, this operation is `GET /user_me` (base URL `https://apius0.processplan.com/api/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-me.md) for the provider-specific parameters and requirements.

