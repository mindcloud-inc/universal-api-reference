# Process Plan: List Valid Process Instance Fields for Process Template Field



```
GET https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/list-valid-process-instance-fields-for-process-template-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Process Plan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/list-valid-process-instance-fields-for-process-template-field?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/list-valid-process-instance-fields-for-process-template-field?${params}`, {
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
| `processTemplateFieldId` | string | no | Process template field ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
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
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
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

## Native endpoint

Through the native Process Plan API, this operation is `GET /process_template_field/:processTemplateFieldId/process_instance_field/list/valid` (base URL `https://apius0.processplan.com/api/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-valid-process-instance-fields-for-process-template-field.md) for the provider-specific parameters and requirements.

