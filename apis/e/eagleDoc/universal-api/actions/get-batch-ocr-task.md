# Eagle Doc: Get Batch OCR Task

Retrieves a batch OCR task from Eagle Doc.

```
GET https://connect.mindcloud.co/v1/universal/eagleDoc/latest/actions/get-batch-ocr-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Eagle Doc `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eagleDoc/latest/actions/get-batch-ocr-task?connectionId=$CONNECTION_ID&taskId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "taskId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eagleDoc/latest/actions/get-batch-ocr-task?${params}`, {
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

```json
{
  "success": true,
  "data": [
    {
      "createdTime": "2026-05-07T12:00:00.000Z",
      "finishedTime": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "messages": {},
      "numberOfFiles": 1,
      "numberOfPages": 1,
      "originalFileNames": [
        "Ava Chen"
      ],
      "queryParams": {
        "configId": "string",
        "docType": "string",
        "endPoint": "string",
        "fromDashboardSaveResult": "string",
        "privacy": "string"
      },
      "status": "string",
      "taskType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdTime` | date |  |
| `finishedTime` | date |  |
| `id` | string |  |
| `messages` | object |  |
| `numberOfFiles` | number |  |
| `numberOfPages` | number |  |
| `originalFileNames[]` | string |  |
| `queryParams.configId` | string |  |
| `queryParams.docType` | string |  |
| `queryParams.endPoint` | string |  |
| `queryParams.fromDashboardSaveResult` | string |  |
| `queryParams.privacy` | string |  |
| `status` | string |  |
| `taskType` | string |  |

## Native endpoint

Through the native Eagle Doc API, this operation is `GET /api/doc/task/v1` (base URL `https://de.eagle-doc.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-batch-ocr-task.md) for the provider-specific parameters and requirements.

