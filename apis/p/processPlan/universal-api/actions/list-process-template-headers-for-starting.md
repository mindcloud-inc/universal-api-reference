# Process Plan: List Process Template Headers For Starting



```
GET https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/list-process-template-headers-for-starting
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Process Plan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/list-process-template-headers-for-starting?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/list-process-template-headers-for-starting?${params}`, {
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
      "process_template_header_list": [
        {
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
| `process_template_header_list[].th_acc_id` | string |  |
| `process_template_header_list[].th_created_date_local` | date |  |
| `process_template_header_list[].th_created_usr_id` | string |  |
| `process_template_header_list[].th_deploy_version_changes` | boolean |  |
| `process_template_header_list[].th_display_start` | boolean |  |
| `process_template_header_list[].th_expire_public_instance_tokens` | boolean |  |
| `process_template_header_list[].th_icon_name` | string |  |
| `process_template_header_list[].th_id` | string |  |
| `process_template_header_list[].th_instance_description_formula` | string |  |
| `process_template_header_list[].th_launch_full_screen` | boolean |  |
| `process_template_header_list[].th_median_duration_seconds` | number |  |
| `process_template_header_list[].th_median_time_seconds` | number |  |
| `process_template_header_list[].th_modified_date_local` | date |  |
| `process_template_header_list[].th_modified_usr_id` | string |  |
| `process_template_header_list[].th_modified_usr_obj.usr_email_address` | string |  |
| `process_template_header_list[].th_modified_usr_obj.usr_first_name` | string |  |
| `process_template_header_list[].th_modified_usr_obj.usr_full_name` | string |  |
| `process_template_header_list[].th_modified_usr_obj.usr_id` | string |  |
| `process_template_header_list[].th_modified_usr_obj.usr_last_name` | string |  |
| `process_template_header_list[].th_modified_usr_obj.usr_profile_pic_url` | string |  |
| `process_template_header_list[].th_name` | string |  |
| `process_template_header_list[].th_personal_task` | boolean |  |
| `process_template_header_list[].th_pg_id` | string |  |
| `process_template_header_list[].th_pg_obj.pg_icon_name` | string |  |
| `process_template_header_list[].th_pg_obj.pg_id` | string |  |
| `process_template_header_list[].th_pg_obj.pg_name` | string |  |
| `process_template_header_list[].th_prevent_delete` | boolean |  |
| `process_template_header_list[].th_primary_dt_publish` | boolean |  |
| `process_template_header_list[].th_priority` | number |  |
| `process_template_header_list[].th_send_launch_response_email` | boolean |  |
| `process_template_header_list[].th_start_tr_id` | string |  |

## Native endpoint

Through the native Process Plan API, this operation is `GET /process_template_header/list/for/starting` (base URL `https://apius0.processplan.com/api/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-process-template-headers-for-starting.md) for the provider-specific parameters and requirements.

