# DocuPipe: Create a Workflow

Creates a workflow in DocuPipe.

```
POST https://connect.mindcloud.co/v1/universal/docuPipe/latest/actions/create-a-workflow
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocuPipe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/docuPipe/latest/actions/create-a-workflow" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/docuPipe/latest/actions/create-a-workflow', {
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
| `standardizeStep` | object | no | This step will always standardize the submitted document through one or more schemas you specify. |
| `standardizeReviewStep` | object | no | This step standardizes the document and immediately reviews every resulting standardization. |
| `classifyStandardizeStep` | object | no | This step allows you to decide on a list of class IDs to classify into, and define which schemas to standardize by, conditional on the classification result. You may choose to only standardize some of the classes, or standardize the same class by multiple schemas. |
| `splitStandardizeStep` | object | no | This step first runs a split operation on the submitted document, then standardizes every resulting sub-document using all schemas provided in `schemaIds`. |
| `splitClassifyStandardizeStep` | object | no | This step runs a split operation on the submitted document, then classifies each resulting sub-document, and finally standardizes any sub-document whose classification matches a provided class-to-schema mapping. |
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

Through the native DocuPipe API, this operation is `POST /workflow/on-submit-document` (base URL `https://app.docupipe.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-a-workflow.md) for the provider-specific parameters and requirements.

