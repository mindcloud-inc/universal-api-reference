# Cradl AI: Create Document

Creates a new document in Cradl AI.

```
POST https://connect.mindcloud.co/v1/universal/cradlAI/latest/actions/create-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cradl AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cradlAI/latest/actions/create-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cradlAI/latest/actions/create-document', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | no | Document name. |
| `description` | string | no | Document description. |
| `datasetId` | string | no | Dataset identifier. |
| `contentType` | string | no | Document content type. |
| `content` | string | no | Document content payload. |
| `groundTruth[]` | array<object> | no | Ground truth labels for the document. |
| `metadata` | object | no | Metadata attached to the document. |
| `consentId` | string | no | Consent identifier for the document. |
| `retentionInDays` | number | no | Retention period in days. |
| `agentRunId` | string | no | Associated agent run identifier. |

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

Through the native Cradl AI API, this operation is `POST /documents` (base URL `https://api.cradl.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-document.md) for the provider-specific parameters and requirements.

