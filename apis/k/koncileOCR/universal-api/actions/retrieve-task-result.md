# Koncile OCR: Retrieve Task Result



```
GET https://connect.mindcloud.co/v1/universal/koncileOCR/latest/actions/retrieve-task-result
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Koncile OCR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/koncileOCR/latest/actions/retrieve-task-result?connectionId=$CONNECTION_ID&task_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "task_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/koncileOCR/latest/actions/retrieve-task-result?${params}`, {
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
| `task_id` | string | yes | The task identifier to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "child_task_ids": [
        "string"
      ],
      "document_id": 1,
      "document_name": "Ava Chen",
      "General_fields": {},
      "Line_fields": {},
      "status": "string",
      "status_message": "string",
      "task_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `child_task_ids` | array<string> | Child task identifiers returned by Koncile for multipart processing. |
| `document_id` | number | The extracted document identifier. |
| `document_name` | string | The uploaded document filename. |
| `General_fields` | object | Fields extracted once per document. |
| `Line_fields` | object | Fields extracted for each line item. |
| `status` | string | The extraction status. |
| `status_message` | string | Additional task status details. |
| `task_id` | string | The Koncile task identifier. |

## Native endpoint

Through the native Koncile OCR API, this operation is `GET /fetch_tasks_results` (base URL `https://api.koncile.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-task-result.md) for the provider-specific parameters and requirements.

