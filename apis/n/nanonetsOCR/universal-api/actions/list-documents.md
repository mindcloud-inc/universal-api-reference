# Nanonets OCR: List Documents



```
GET https://connect.mindcloud.co/v1/universal/nanonetsOCR/latest/actions/list-documents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nanonets OCR `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nanonetsOCR/latest/actions/list-documents?connectionId=$CONNECTION_ID&limit=25&offset=0&workflowId=Select%20a%20workflow" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "workflowId": "Select a workflow"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nanonetsOCR/latest/actions/list-documents?${params}`, {
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
| `workflowId` | list | yes | Workflow identifier. Example: `Select a workflow`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "documents": [
        {
          "documentId": "string",
          "originalDocumentName": "Ava Chen",
          "pages": [
            {
              "data": {
                "fields": {},
                "tables": {}
              },
              "imageUrl": "https://example.com",
              "pageId": "string",
              "pageNumber": 1
            }
          ],
          "rawDocumentUrl": "https://example.com",
          "status": "string",
          "uploadedAt": "string",
          "verificationStage": "string",
          "verificationStatus": "string"
        }
      ],
      "pageNo": 1,
      "pageSize": 1,
      "totalCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `documents[].documentId` | string |  |
| `documents[].originalDocumentName` | string |  |
| `documents[].pages[].data.fields` | object |  |
| `documents[].pages[].data.tables` | object |  |
| `documents[].pages[].imageUrl` | string |  |
| `documents[].pages[].pageId` | string |  |
| `documents[].pages[].pageNumber` | number |  |
| `documents[].rawDocumentUrl` | string |  |
| `documents[].status` | string |  |
| `documents[].uploadedAt` | string |  |
| `documents[].verificationStage` | string |  |
| `documents[].verificationStatus` | string |  |
| `pageNo` | number |  |
| `pageSize` | number |  |
| `totalCount` | number |  |

## Native endpoint

Through the native Nanonets OCR API, this operation is `GET /workflows/:workflow_id/documents` (base URL `https://app.nanonets.com/api/v4`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-documents.md) for the provider-specific parameters and requirements.

