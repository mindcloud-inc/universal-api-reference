# Claid AI: Get Batch Image Edit Results

Retrieves batch image edit results from Claid AI.

```
GET https://connect.mindcloud.co/v1/universal/claidAI/latest/actions/get-batch-image-edit-results
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Claid AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/claidAI/latest/actions/get-batch-image-edit-results?connectionId=$CONNECTION_ID&taskId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "taskId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/claidAI/latest/actions/get-batch-image-edit-results?${params}`, {
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
| `taskId` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "errors": [
        {}
      ],
      "id": 1,
      "request": {},
      "results": [
        {}
      ],
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date | Request creation timestamp. |
| `errors` | array<object> | Processing errors, if any. |
| `id` | number | Task identifier. |
| `request` | object | Echoed request payload. |
| `results` | array<object> | Batch result rows containing input and output object pairs. |
| `status` | string | Current processing status. |

## Native endpoint

Through the native Claid AI API, this operation is `GET image/edit/batch/:task_id` (base URL `https://api.claid.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-batch-image-edit-results.md) for the provider-specific parameters and requirements.

