# Process Plan: Get Process Template Header for Applies in Standard Operation Procedure Template



```
GET https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/get-process-template-header-for-applies-in-standard-operation-procedure-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Process Plan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/get-process-template-header-for-applies-in-standard-operation-procedure-template?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/get-process-template-header-for-applies-in-standard-operation-procedure-template?${params}`, {
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
| `sopTemplateId` | string | no | Sop template ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "developer_message": "string",
      "message_number": 1,
      "sop_acc_id": "string",
      "sop_created_date_local": "2026-05-07T12:00:00.000Z",
      "sop_created_usr_id": "string",
      "sop_html": "string",
      "sop_id": "string",
      "sop_modified_date_local": "2026-05-07T12:00:00.000Z",
      "sop_modified_usr_id": "string",
      "sop_name": "Ava Chen",
      "user_message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `developer_message` | string |  |
| `message_number` | number |  |
| `sop_acc_id` | string |  |
| `sop_created_date_local` | date |  |
| `sop_created_usr_id` | string |  |
| `sop_html` | string |  |
| `sop_id` | string |  |
| `sop_modified_date_local` | date |  |
| `sop_modified_usr_id` | string |  |
| `sop_name` | string |  |
| `user_message` | string |  |

## Native endpoint

Through the native Process Plan API, this operation is `GET /sop_template/:sopTemplateId/apply/process_template_header/:processTemplateHeaderId` (base URL `https://apius0.processplan.com/api/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-process-template-header-for-applies-in-standard-operation-procedure-template.md) for the provider-specific parameters and requirements.

