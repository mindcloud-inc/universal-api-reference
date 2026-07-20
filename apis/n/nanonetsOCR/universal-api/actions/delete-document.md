# Nanonets OCR: Delete Document



```
DELETE https://connect.mindcloud.co/v1/universal/nanonetsOCR/latest/actions/delete-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nanonets OCR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/nanonetsOCR/latest/actions/delete-document?connectionId=$CONNECTION_ID&workflowId=string&documentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workflowId": "string",
  "documentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nanonetsOCR/latest/actions/delete-document?${params}`, {
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
| `workflowId` | list | yes | Workflow ID that owns the document. |
| `documentId` | string | yes | Document ID to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Provider success message after the document is deleted. |

## Native endpoint

Through the native Nanonets OCR API, this operation is `DELETE /workflows/:workflow_id/documents/:document_id` (base URL `https://app.nanonets.com/api/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-document.md) for the provider-specific parameters and requirements.

