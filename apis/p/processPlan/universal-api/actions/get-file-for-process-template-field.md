# Process Plan: Get File for Process Template Field



```
GET https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/get-file-for-process-template-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Process Plan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/get-file-for-process-template-field?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/get-file-for-process-template-field?${params}`, {
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
| `fileId` | string | no | File ID. |
| `processTemplateFieldId` | string | no | Process template field ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "th_fl_acc_id": "string",
      "th_fl_created_date_local": "2026-05-07T12:00:00.000Z",
      "th_fl_created_usr_id": "string",
      "th_fl_fl_id": "string",
      "th_fl_fl_obj": {
        "fl_acc_id": "string",
        "fl_authenticated_url": "https://example.com",
        "fl_created_date_local": "2026-05-07T12:00:00.000Z",
        "fl_created_usr_id": "string",
        "fl_id": "string",
        "fl_modified_date_local": "2026-05-07T12:00:00.000Z",
        "fl_modified_usr_id": "string",
        "fl_name": "Ava Chen",
        "fl_pp_logo": true,
        "fl_private_url": "https://example.com",
        "fl_type": 1,
        "fl_url": "https://example.com"
      },
      "th_fl_th_id": "string",
      "th_fl_th_obj": {
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
        "th_launch_id_list": [
          "string"
        ],
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
      "th_fl_tt_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `th_fl_acc_id` | string |  |
| `th_fl_created_date_local` | date |  |
| `th_fl_created_usr_id` | string |  |
| `th_fl_fl_id` | string |  |
| `th_fl_fl_obj.fl_acc_id` | string |  |
| `th_fl_fl_obj.fl_authenticated_url` | string |  |
| `th_fl_fl_obj.fl_created_date_local` | date |  |
| `th_fl_fl_obj.fl_created_usr_id` | string |  |
| `th_fl_fl_obj.fl_id` | string |  |
| `th_fl_fl_obj.fl_modified_date_local` | date |  |
| `th_fl_fl_obj.fl_modified_usr_id` | string |  |
| `th_fl_fl_obj.fl_name` | string |  |
| `th_fl_fl_obj.fl_pp_logo` | boolean |  |
| `th_fl_fl_obj.fl_private_url` | string |  |
| `th_fl_fl_obj.fl_type` | number |  |
| `th_fl_fl_obj.fl_url` | string |  |
| `th_fl_th_id` | string |  |
| `th_fl_th_obj.th_acc_id` | string |  |
| `th_fl_th_obj.th_created_date_local` | date |  |
| `th_fl_th_obj.th_created_usr_id` | string |  |
| `th_fl_th_obj.th_deploy_version_changes` | boolean |  |
| `th_fl_th_obj.th_display_start` | boolean |  |
| `th_fl_th_obj.th_expire_public_instance_tokens` | boolean |  |
| `th_fl_th_obj.th_icon_name` | string |  |
| `th_fl_th_obj.th_id` | string |  |
| `th_fl_th_obj.th_instance_description_formula` | string |  |
| `th_fl_th_obj.th_launch_full_screen` | boolean |  |
| `th_fl_th_obj.th_launch_id_list[]` | string |  |
| `th_fl_th_obj.th_median_duration_seconds` | number |  |
| `th_fl_th_obj.th_median_time_seconds` | number |  |
| `th_fl_th_obj.th_modified_date_local` | date |  |
| `th_fl_th_obj.th_modified_usr_id` | string |  |
| `th_fl_th_obj.th_name` | string |  |
| `th_fl_th_obj.th_personal_task` | boolean |  |
| `th_fl_th_obj.th_pg_id` | string |  |
| `th_fl_th_obj.th_prevent_delete` | boolean |  |
| `th_fl_th_obj.th_primary_dt_publish` | boolean |  |
| `th_fl_th_obj.th_priority` | number |  |
| `th_fl_th_obj.th_send_launch_response_email` | boolean |  |
| `th_fl_th_obj.th_start_tr_id` | string |  |
| `th_fl_tt_id` | string |  |

## Native endpoint

Through the native Process Plan API, this operation is `GET /process_template_field/:processTemplateFieldId/file/:fileId` (base URL `https://apius0.processplan.com/api/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-file-for-process-template-field.md) for the provider-specific parameters and requirements.

