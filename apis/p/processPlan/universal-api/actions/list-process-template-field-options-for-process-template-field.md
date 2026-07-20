# Process Plan: List Process Template Field Options for Process Template Field



```
GET https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/list-process-template-field-options-for-process-template-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Process Plan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/list-process-template-field-options-for-process-template-field?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/list-process-template-field-options-for-process-template-field?${params}`, {
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
      "process_template_field_obj": {
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
        "tf_unique": true,
        "tf_value_formula": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `process_template_field_obj.tf_acc_id` | string |  |
| `process_template_field_obj.tf_calculate_type` | number |  |
| `process_template_field_obj.tf_created_date_local` | date |  |
| `process_template_field_obj.tf_created_usr_id` | string |  |
| `process_template_field_obj.tf_display_at_start` | boolean |  |
| `process_template_field_obj.tf_fl_analysis_type` | number |  |
| `process_template_field_obj.tf_format_type` | number |  |
| `process_template_field_obj.tf_id` | string |  |
| `process_template_field_obj.tf_modified_date_local` | date |  |
| `process_template_field_obj.tf_modified_usr_id` | string |  |
| `process_template_field_obj.tf_name` | string |  |
| `process_template_field_obj.tf_public_read_only` | boolean |  |
| `process_template_field_obj.tf_read_only` | boolean |  |
| `process_template_field_obj.tf_required` | boolean |  |
| `process_template_field_obj.tf_required_on_x` | boolean |  |
| `process_template_field_obj.tf_secure` | boolean |  |
| `process_template_field_obj.tf_share_with_parent` | boolean |  |
| `process_template_field_obj.tf_sort_num` | number |  |
| `process_template_field_obj.tf_th_id` | string |  |
| `process_template_field_obj.tf_type` | number |  |
| `process_template_field_obj.tf_unique` | boolean |  |
| `process_template_field_obj.tf_value_formula` | string |  |

## Native endpoint

Through the native Process Plan API, this operation is `GET /process_template_field/:processTemplateFieldId/process_template_field_option/list` (base URL `https://apius0.processplan.com/api/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-process-template-field-options-for-process-template-field.md) for the provider-specific parameters and requirements.

