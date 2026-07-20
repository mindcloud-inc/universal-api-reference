# Cradl AI: Update Document

Updates an existing document in Cradl AI.

```
PUT https://connect.mindcloud.co/v1/universal/cradlAI/latest/actions/update-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cradl AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/cradlAI/latest/actions/update-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "documentId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cradlAI/latest/actions/update-document', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "documentId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `documentId` | string | yes | Identifier of the document to update. |
| `name` | string | no | Updated document name. |
| `description` | string | no | Updated document description. |
| `datasetId` | string | no | Updated dataset identifier. |
| `groundTruth[]` | array<object> | no | Updated ground truth labels for the document. |
| `metadata` | object | no | Updated metadata attached to the document. |
| `retentionInDays` | number | no | Updated retention period in days. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "agentRunId": "string",
      "annotationFileUrl": "https://example.com",
      "consentId": "string",
      "content": "string",
      "contentMD5": "string",
      "contentType": "string",
      "createdBy": "string",
      "createdTime": "2026-05-07T12:00:00.000Z",
      "datasetId": "string",
      "description": "string",
      "documentId": "string",
      "fileUrl": "https://example.com",
      "groundTruth": [
        {}
      ],
      "metadata": {},
      "name": "Ava Chen",
      "ocrFileUrl": "https://example.com",
      "retentionInDays": 1,
      "updatedBy": "string",
      "updatedTime": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agentRunId` | string |  |
| `annotationFileUrl` | string |  |
| `consentId` | string |  |
| `content` | string |  |
| `contentMD5` | string |  |
| `contentType` | string |  |
| `createdBy` | string |  |
| `createdTime` | date |  |
| `datasetId` | string |  |
| `description` | string |  |
| `documentId` | string |  |
| `fileUrl` | string |  |
| `groundTruth` | array<object> |  |
| `metadata` | object |  |
| `name` | string |  |
| `ocrFileUrl` | string |  |
| `retentionInDays` | number |  |
| `updatedBy` | string |  |
| `updatedTime` | date |  |

## Native endpoint

Through the native Cradl AI API, this operation is `PATCH /documents/:documentId` (base URL `https://api.cradl.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-document.md) for the provider-specific parameters and requirements.

