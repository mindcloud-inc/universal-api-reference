# Process Plan: List Process Template Task Responses for Process Template Task in Process Template Header



```
GET https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/list-process-template-task-responses-for-process-template-task-in-process-template-header
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Process Plan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/list-process-template-task-responses-for-process-template-task-in-process-template-header?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/list-process-template-task-responses-for-process-template-task-in-process-template-header?${params}`, {
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
| `processTemplateTaskId` | string | no | Process template task ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
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
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
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
| `process_template_response_list[].tr_max_selections` | number |  |
| `process_template_response_list[].tr_modified_date_local` | date |  |
| `process_template_response_list[].tr_modified_usr_id` | string |  |
| `process_template_response_list[].tr_name` | string |  |
| `process_template_response_list[].tr_next_task_delay_seconds` | number |  |
| `process_template_response_list[].tr_note_required` | boolean |  |
| `process_template_response_list[].tr_process_in_background` | boolean |  |
| `process_template_response_list[].tr_sort_num` | number |  |
| `process_template_response_list[].tr_universal_response` | boolean |  |

## Native endpoint

Through the native Process Plan API, this operation is `GET /process_template_header/:processTemplateHeaderId/process_template_task/:processTemplateTaskId/process_template_response/list` (base URL `https://apius0.processplan.com/api/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-process-template-task-responses-for-process-template-task-in-process-template-header.md) for the provider-specific parameters and requirements.

