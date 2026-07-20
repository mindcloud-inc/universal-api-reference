# DocuPanda - Document Understanding: Create a Workflow

Creates an on-submit workflow in DocuPanda.

```
POST https://connect.mindcloud.co/v1/universal/docuPandaDocumentUnderstanding/latest/actions/post-workflow-on-submit-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocuPanda - Document Understanding `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/docuPandaDocumentUnderstanding/latest/actions/post-workflow-on-submit-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/docuPandaDocumentUnderstanding/latest/actions/post-workflow-on-submit-document', {
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
| `classifyStandardizeStep` | object | no |  |
| `splitClassifyStandardizeStep` | object | no |  |
| `splitStandardizeStep` | object | no |  |
| `standardizeReviewStep` | object | no |  |
| `standardizeStep` | object | no |  |
| `workflowName` | string | no | Optionally name your workflow |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true,
      "workflowId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean | Whether the workflow was successfully created |
| `workflowId` | string | The id of the workflow that was created. Call POST `/document` with this workflowId to run it |

## Native endpoint

Through the native DocuPanda - Document Understanding API, this operation is `POST /workflow/on-submit-document` (base URL `https://app.docupipe.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/post-workflow-on-submit-document.md) for the provider-specific parameters and requirements.

