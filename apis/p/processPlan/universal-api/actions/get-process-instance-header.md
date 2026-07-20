# Process Plan: Get Process Instance Header



```
GET https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/get-process-instance-header
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Process Plan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/get-process-instance-header?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/get-process-instance-header?${params}`, {
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
| `processInstanceHeaderId` | string | no | Process instance header ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ih_acc_id": "string",
      "ih_actual_duration_seconds": 1,
      "ih_actual_time_seconds": 1,
      "ih_apply_version_changes": true,
      "ih_created_date_local": "2026-05-07T12:00:00.000Z",
      "ih_created_usr_id": "string",
      "ih_created_usr_obj": {
        "usr_email_address": "ava@example.com",
        "usr_first_name": "Ava",
        "usr_full_name": "Ava Chen",
        "usr_id": "string",
        "usr_last_name": "Chen",
        "usr_profile_pic_url": "https://example.com"
      },
      "ih_favorable_rating": 1,
      "ih_id": "string",
      "ih_instance_description": "string",
      "ih_modified_date_local": "2026-05-07T12:00:00.000Z",
      "ih_modified_usr_id": "string",
      "ih_pending_it_id": "string",
      "ih_pending_it_obj": {
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
        "it_id": "string",
        "it_ih_id": "string",
        "it_name": "Ava Chen",
        "it_notes": "string",
        "it_tag_text": "string",
        "it_tt_id": "string"
      },
      "ih_personal_task": true,
      "ih_primary_dt_published": true,
      "ih_progress_date_local": "2026-05-07T12:00:00.000Z",
      "ih_progress_percentage": 1,
      "ih_progress_usr_id": "string",
      "ih_test_mode": true,
      "ih_th_id": "string",
      "ih_th_obj": {
        "th_icon_name": "Ava Chen",
        "th_id": "string",
        "th_name": "Ava Chen",
        "th_pg_obj": {
          "pg_icon_name": "Ava Chen",
          "pg_id": "string",
          "pg_name": "Ava Chen"
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ih_acc_id` | string |  |
| `ih_actual_duration_seconds` | number |  |
| `ih_actual_time_seconds` | number |  |
| `ih_apply_version_changes` | boolean |  |
| `ih_created_date_local` | date |  |
| `ih_created_usr_id` | string |  |
| `ih_created_usr_obj.usr_email_address` | string |  |
| `ih_created_usr_obj.usr_first_name` | string |  |
| `ih_created_usr_obj.usr_full_name` | string |  |
| `ih_created_usr_obj.usr_id` | string |  |
| `ih_created_usr_obj.usr_last_name` | string |  |
| `ih_created_usr_obj.usr_profile_pic_url` | string |  |
| `ih_favorable_rating` | number |  |
| `ih_id` | string |  |
| `ih_instance_description` | string |  |
| `ih_modified_date_local` | date |  |
| `ih_modified_usr_id` | string |  |
| `ih_pending_it_id` | string |  |
| `ih_pending_it_obj.it_assigned_name` | string |  |
| `ih_pending_it_obj.it_assigned_ug_id` | string |  |
| `ih_pending_it_obj.it_assigned_ug_obj.ug_id` | string |  |
| `ih_pending_it_obj.it_assigned_ug_obj.ug_name` | string |  |
| `ih_pending_it_obj.it_assigned_usr_id` | string |  |
| `ih_pending_it_obj.it_assigned_usr_obj.usr_email_address` | string |  |
| `ih_pending_it_obj.it_assigned_usr_obj.usr_first_name` | string |  |
| `ih_pending_it_obj.it_assigned_usr_obj.usr_full_name` | string |  |
| `ih_pending_it_obj.it_assigned_usr_obj.usr_id` | string |  |
| `ih_pending_it_obj.it_assigned_usr_obj.usr_last_name` | string |  |
| `ih_pending_it_obj.it_assigned_usr_obj.usr_profile_pic_url` | string |  |
| `ih_pending_it_obj.it_id` | string |  |
| `ih_pending_it_obj.it_ih_id` | string |  |
| `ih_pending_it_obj.it_name` | string |  |
| `ih_pending_it_obj.it_notes` | string |  |
| `ih_pending_it_obj.it_tag_text` | string |  |
| `ih_pending_it_obj.it_tt_id` | string |  |
| `ih_personal_task` | boolean |  |
| `ih_primary_dt_published` | boolean |  |
| `ih_progress_date_local` | date |  |
| `ih_progress_percentage` | number |  |
| `ih_progress_usr_id` | string |  |
| `ih_test_mode` | boolean |  |
| `ih_th_id` | string |  |
| `ih_th_obj.th_icon_name` | string |  |
| `ih_th_obj.th_id` | string |  |
| `ih_th_obj.th_name` | string |  |
| `ih_th_obj.th_pg_obj.pg_icon_name` | string |  |
| `ih_th_obj.th_pg_obj.pg_id` | string |  |
| `ih_th_obj.th_pg_obj.pg_name` | string |  |

## Native endpoint

Through the native Process Plan API, this operation is `GET /process_instance_header/:processInstanceHeaderId` (base URL `https://apius0.processplan.com/api/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-process-instance-header.md) for the provider-specific parameters and requirements.

