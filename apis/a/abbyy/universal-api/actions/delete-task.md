# Abbyy: Delete Task

Deletes an existing OCR task from ABBYY Cloud OCR SDK.

```
DELETE https://connect.mindcloud.co/v1/universal/abbyy/latest/actions/delete-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Abbyy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/abbyy/latest/actions/delete-task?connectionId=$CONNECTION_ID&taskId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "taskId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/abbyy/latest/actions/delete-task?${params}`, {
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
| `taskId` | string | yes | ABBYY OCR task identifier to delete. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Abbyy API returns.

## Native endpoint

Through the native Abbyy API, this operation is `POST /v2/deleteTask` (base URL `https://cloud-westus.ocrsdk.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-task.md) for the provider-specific parameters and requirements.

