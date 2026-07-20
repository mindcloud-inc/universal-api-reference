# Eagle Doc: Create Finance Document Batch OCR Task

Creates a finance document batch OCR task in Eagle Doc.

```
POST https://connect.mindcloud.co/v1/universal/eagleDoc/latest/actions/create-finance-document-batch-ocr-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Eagle Doc `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/eagleDoc/latest/actions/create-finance-document-batch-ocr-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eagleDoc/latest/actions/create-finance-document-batch-ocr-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "file": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `docType` | string | no | Document type used for finance batch extraction |
| `file` | file | yes | Archive file that contains the finance batch input files |
| `fullText` | boolean | no | Include the extracted full text by page for each result |
| `polygon` | boolean | no | Include polygon coordinates in each extracted result |
| `privacy` | boolean | no | Whether Eagle Doc should avoid storing the uploaded file |

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
        "docType": "string",
        "endPoint": "string",
        "includeFullText": "string",
        "includePolygon": "string",
        "includeSignature": "string",
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
| `queryParams.docType` | string |  |
| `queryParams.endPoint` | string |  |
| `queryParams.includeFullText` | string |  |
| `queryParams.includePolygon` | string |  |
| `queryParams.includeSignature` | string |  |
| `queryParams.privacy` | string |  |
| `status` | string |  |
| `taskType` | string |  |

## Native endpoint

Through the native Eagle Doc API, this operation is `POST /api/finance/extract/batch/task/v1` (base URL `https://de.eagle-doc.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-finance-document-batch-ocr-task.md) for the provider-specific parameters and requirements.

