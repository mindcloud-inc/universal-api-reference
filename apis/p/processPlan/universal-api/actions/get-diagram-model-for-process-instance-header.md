# Process Plan: Get Diagram Model for Process Instance Header



```
GET https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/get-diagram-model-for-process-instance-header
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Process Plan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/get-diagram-model-for-process-instance-header?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/get-diagram-model-for-process-instance-header?${params}`, {
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
      "message_obj": {
        "msg_count": 1
      },
      "process_diagram": {
        "linkDataArray": [
          {
            "from": "https://example.com",
            "loopBack": true,
            "to": "https://example.com"
          }
        ],
        "nodeDataArray": [
          {
            "assignedToUserGroupID": "string",
            "assignedToUserID": "string",
            "attachmentExists": true,
            "automatedActionExists": true,
            "backgroundColor": "string",
            "cancelProcessExists": true,
            "category": "string",
            "checklistExists": true,
            "dateExists": true,
            "executionStatus": "string",
            "foregroundColor": "string",
            "instanceTaskID": "string",
            "isEditable": true,
            "isResponseAllowed": true,
            "key": "string",
            "manuallyStarted": true,
            "milestoneExists": true,
            "noPathValidation": true,
            "openInstanceTask": true,
            "openTemplateResponse": true,
            "openTemplateTask": true,
            "profilePictureURL": "https://example.com",
            "publicTask": true,
            "sourceID": "string",
            "status": "string",
            "subText": "string",
            "templateID": "string",
            "templateTaskID": "string",
            "text": "string"
          }
        ]
      },
      "process_instance_field_list": [
        {
          "if_acc_id": "string",
          "if_created_date_local": "2026-05-07T12:00:00.000Z",
          "if_created_usr_id": "string",
          "if_id": "string",
          "if_ih_id": "string",
          "if_modified_date_local": "2026-05-07T12:00:00.000Z",
          "if_modified_usr_id": "string",
          "if_postback_on_change": true,
          "if_text": "string",
          "if_tf_id": "string",
          "if_tf_obj": {
            "tf_id": "string",
            "tf_name": "Ava Chen",
            "tf_required": true,
            "tf_type": 1
          },
          "if_th_id": "string",
          "if_ui_hide": true,
          "if_ui_read_only": true,
          "if_ui_required": true,
          "if_value": "string",
          "if_value_numeric": 1
        }
      ],
      "process_instance_header_obj": {
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
      },
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
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message_obj.msg_count` | number |  |
| `process_diagram.linkDataArray[].from` | string |  |
| `process_diagram.linkDataArray[].loopBack` | boolean |  |
| `process_diagram.linkDataArray[].to` | string |  |
| `process_diagram.nodeDataArray[].assignedToUserGroupID` | string |  |
| `process_diagram.nodeDataArray[].assignedToUserID` | string |  |
| `process_diagram.nodeDataArray[].attachmentExists` | boolean |  |
| `process_diagram.nodeDataArray[].automatedActionExists` | boolean |  |
| `process_diagram.nodeDataArray[].backgroundColor` | string |  |
| `process_diagram.nodeDataArray[].cancelProcessExists` | boolean |  |
| `process_diagram.nodeDataArray[].category` | string |  |
| `process_diagram.nodeDataArray[].checklistExists` | boolean |  |
| `process_diagram.nodeDataArray[].dateExists` | boolean |  |
| `process_diagram.nodeDataArray[].executionStatus` | string |  |
| `process_diagram.nodeDataArray[].foregroundColor` | string |  |
| `process_diagram.nodeDataArray[].instanceTaskID` | string |  |
| `process_diagram.nodeDataArray[].isEditable` | boolean |  |
| `process_diagram.nodeDataArray[].isResponseAllowed` | boolean |  |
| `process_diagram.nodeDataArray[].key` | string |  |
| `process_diagram.nodeDataArray[].manuallyStarted` | boolean |  |
| `process_diagram.nodeDataArray[].milestoneExists` | boolean |  |
| `process_diagram.nodeDataArray[].noPathValidation` | boolean |  |
| `process_diagram.nodeDataArray[].openInstanceTask` | boolean |  |
| `process_diagram.nodeDataArray[].openTemplateResponse` | boolean |  |
| `process_diagram.nodeDataArray[].openTemplateTask` | boolean |  |
| `process_diagram.nodeDataArray[].profilePictureURL` | string |  |
| `process_diagram.nodeDataArray[].publicTask` | boolean |  |
| `process_diagram.nodeDataArray[].sourceID` | string |  |
| `process_diagram.nodeDataArray[].status` | string |  |
| `process_diagram.nodeDataArray[].subText` | string |  |
| `process_diagram.nodeDataArray[].templateID` | string |  |
| `process_diagram.nodeDataArray[].templateTaskID` | string |  |
| `process_diagram.nodeDataArray[].text` | string |  |
| `process_instance_field_list[].if_acc_id` | string |  |
| `process_instance_field_list[].if_created_date_local` | date |  |
| `process_instance_field_list[].if_created_usr_id` | string |  |
| `process_instance_field_list[].if_id` | string |  |
| `process_instance_field_list[].if_ih_id` | string |  |
| `process_instance_field_list[].if_modified_date_local` | date |  |
| `process_instance_field_list[].if_modified_usr_id` | string |  |
| `process_instance_field_list[].if_postback_on_change` | boolean |  |
| `process_instance_field_list[].if_text` | string |  |
| `process_instance_field_list[].if_tf_id` | string |  |
| `process_instance_field_list[].if_tf_obj.tf_id` | string |  |
| `process_instance_field_list[].if_tf_obj.tf_name` | string |  |
| `process_instance_field_list[].if_tf_obj.tf_required` | boolean |  |
| `process_instance_field_list[].if_tf_obj.tf_type` | number |  |
| `process_instance_field_list[].if_th_id` | string |  |
| `process_instance_field_list[].if_ui_hide` | boolean |  |
| `process_instance_field_list[].if_ui_read_only` | boolean |  |
| `process_instance_field_list[].if_ui_required` | boolean |  |
| `process_instance_field_list[].if_value` | string |  |
| `process_instance_field_list[].if_value_numeric` | number |  |
| `process_instance_header_obj.ih_acc_id` | string |  |
| `process_instance_header_obj.ih_actual_duration_seconds` | number |  |
| `process_instance_header_obj.ih_actual_time_seconds` | number |  |
| `process_instance_header_obj.ih_apply_version_changes` | boolean |  |
| `process_instance_header_obj.ih_created_date_local` | date |  |
| `process_instance_header_obj.ih_created_usr_id` | string |  |
| `process_instance_header_obj.ih_created_usr_obj.usr_email_address` | string |  |
| `process_instance_header_obj.ih_created_usr_obj.usr_first_name` | string |  |
| `process_instance_header_obj.ih_created_usr_obj.usr_full_name` | string |  |
| `process_instance_header_obj.ih_created_usr_obj.usr_id` | string |  |
| `process_instance_header_obj.ih_created_usr_obj.usr_last_name` | string |  |
| `process_instance_header_obj.ih_created_usr_obj.usr_profile_pic_url` | string |  |
| `process_instance_header_obj.ih_favorable_rating` | number |  |
| `process_instance_header_obj.ih_id` | string |  |
| `process_instance_header_obj.ih_instance_description` | string |  |
| `process_instance_header_obj.ih_modified_date_local` | date |  |
| `process_instance_header_obj.ih_modified_usr_id` | string |  |
| `process_instance_header_obj.ih_pending_it_id` | string |  |
| `process_instance_header_obj.ih_pending_it_obj.it_assigned_name` | string |  |
| `process_instance_header_obj.ih_pending_it_obj.it_assigned_ug_id` | string |  |
| `process_instance_header_obj.ih_pending_it_obj.it_assigned_ug_obj.ug_id` | string |  |
| `process_instance_header_obj.ih_pending_it_obj.it_assigned_ug_obj.ug_name` | string |  |
| `process_instance_header_obj.ih_pending_it_obj.it_assigned_usr_id` | string |  |
| `process_instance_header_obj.ih_pending_it_obj.it_assigned_usr_obj.usr_email_address` | string |  |
| `process_instance_header_obj.ih_pending_it_obj.it_assigned_usr_obj.usr_first_name` | string |  |
| `process_instance_header_obj.ih_pending_it_obj.it_assigned_usr_obj.usr_full_name` | string |  |
| `process_instance_header_obj.ih_pending_it_obj.it_assigned_usr_obj.usr_id` | string |  |
| `process_instance_header_obj.ih_pending_it_obj.it_assigned_usr_obj.usr_last_name` | string |  |
| `process_instance_header_obj.ih_pending_it_obj.it_assigned_usr_obj.usr_profile_pic_url` | string |  |
| `process_instance_header_obj.ih_pending_it_obj.it_id` | string |  |
| `process_instance_header_obj.ih_pending_it_obj.it_ih_id` | string |  |
| `process_instance_header_obj.ih_pending_it_obj.it_name` | string |  |
| `process_instance_header_obj.ih_pending_it_obj.it_notes` | string |  |
| `process_instance_header_obj.ih_pending_it_obj.it_tag_text` | string |  |
| `process_instance_header_obj.ih_pending_it_obj.it_tt_id` | string |  |
| `process_instance_header_obj.ih_personal_task` | boolean |  |
| `process_instance_header_obj.ih_primary_dt_published` | boolean |  |
| `process_instance_header_obj.ih_progress_date_local` | date |  |
| `process_instance_header_obj.ih_progress_percentage` | number |  |
| `process_instance_header_obj.ih_progress_usr_id` | string |  |
| `process_instance_header_obj.ih_test_mode` | boolean |  |
| `process_instance_header_obj.ih_th_id` | string |  |
| `process_instance_header_obj.ih_th_obj.th_icon_name` | string |  |
| `process_instance_header_obj.ih_th_obj.th_id` | string |  |
| `process_instance_header_obj.ih_th_obj.th_name` | string |  |
| `process_instance_header_obj.ih_th_obj.th_pg_obj.pg_icon_name` | string |  |
| `process_instance_header_obj.ih_th_obj.th_pg_obj.pg_id` | string |  |
| `process_instance_header_obj.ih_th_obj.th_pg_obj.pg_name` | string |  |
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
| `process_template_header_obj.th_launch_id_list[]` | string |  |
| `process_template_header_obj.th_median_duration_seconds` | number |  |
| `process_template_header_obj.th_median_time_seconds` | number |  |
| `process_template_header_obj.th_modified_date_local` | date |  |
| `process_template_header_obj.th_modified_usr_id` | string |  |
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

## Native endpoint

Through the native Process Plan API, this operation is `GET /process_instance_header/:processInstanceHeaderId/diagram_model` (base URL `https://apius0.processplan.com/api/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-diagram-model-for-process-instance-header.md) for the provider-specific parameters and requirements.

