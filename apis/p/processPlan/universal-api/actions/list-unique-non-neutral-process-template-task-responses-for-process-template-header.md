# Process Plan: List Unique Non Neutral Process Template Task Responses for Process Template Header



```
GET https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/list-unique-non-neutral-process-template-task-responses-for-process-template-header
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Process Plan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/list-unique-non-neutral-process-template-task-responses-for-process-template-header?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/list-unique-non-neutral-process-template-task-responses-for-process-template-header?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "result_list": [
        {
          "developer_message": "string",
          "http_status_code": 1,
          "message_number": 1
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
| `result_list[].developer_message` | string |  |
| `result_list[].http_status_code` | number |  |
| `result_list[].message_number` | number |  |

## Native endpoint

Through the native Process Plan API, this operation is `GET /process_template_header/:processTemplateHeaderId/unique/process_template_response/list/non_neutral` (base URL `https://apius0.processplan.com/api/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-unique-non-neutral-process-template-task-responses-for-process-template-header.md) for the provider-specific parameters and requirements.

