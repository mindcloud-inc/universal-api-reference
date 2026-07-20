# DocuPanda - Document Understanding: List your Workflows

Retrieves workflows from DocuPanda.

```
GET https://connect.mindcloud.co/v1/universal/docuPandaDocumentUnderstanding/latest/actions/list-workflows
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocuPanda - Document Understanding `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docuPandaDocumentUnderstanding/latest/actions/list-workflows?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docuPandaDocumentUnderstanding/latest/actions/list-workflows?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "workflowContents": {},
      "workflowId": "string",
      "workflowName": "Ava Chen",
      "workflowTrigger": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `workflowContents` | object | The details of the workflow. Currently this will always be a dictionary with key being 'step' and value being StandardizeStep, StandardizeReviewStep, ClassifyStandardizeStep, SplitStandardizeStep, or SplitClassifyStandardizeStep. |
| `workflowId` | string | Unique identifier of the workflow. |
| `workflowName` | string | Name of the workflow. |
| `workflowTrigger` | object | The trigger that activates the workflow. |

## Native endpoint

Through the native DocuPanda - Document Understanding API, this operation is `GET /workflows` (base URL `https://app.docupipe.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-workflows.md) for the provider-specific parameters and requirements.

