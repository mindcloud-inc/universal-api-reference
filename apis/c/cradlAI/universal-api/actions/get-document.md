# Cradl AI: Get Document

Retrieves a document from Cradl AI.

```
GET https://connect.mindcloud.co/v1/universal/cradlAI/latest/actions/get-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cradl AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cradlAI/latest/actions/get-document?connectionId=$CONNECTION_ID&documentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "documentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cradlAI/latest/actions/get-document?${params}`, {
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
| `documentId` | string | yes | Identifier of the document. |

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

Through the native Cradl AI API, this operation is `GET /documents/:documentId` (base URL `https://api.cradl.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-document.md) for the provider-specific parameters and requirements.

