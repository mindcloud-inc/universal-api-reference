# Eagle Doc: Delete Batch OCR Task

Deletes an existing batch OCR task from Eagle Doc.

```
DELETE https://connect.mindcloud.co/v1/universal/eagleDoc/latest/actions/delete-batch-ocr-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Eagle Doc `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/eagleDoc/latest/actions/delete-batch-ocr-task?connectionId=$CONNECTION_ID&taskId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "taskId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eagleDoc/latest/actions/delete-batch-ocr-task?${params}`, {
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
| `taskId` | string | yes | Batch task ID returned by Eagle Doc when the batch job was created |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Eagle Doc API returns.

## Native endpoint

Through the native Eagle Doc API, this operation is `DELETE /api/doc/task/v1` (base URL `https://de.eagle-doc.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-batch-ocr-task.md) for the provider-specific parameters and requirements.

