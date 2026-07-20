# DocuPanda - Document Understanding: Delete a Workflow

Deletes an existing workflow from DocuPanda.

```
DELETE https://connect.mindcloud.co/v1/universal/docuPandaDocumentUnderstanding/latest/actions/delete-workflow
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocuPanda - Document Understanding `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/docuPandaDocumentUnderstanding/latest/actions/delete-workflow?connectionId=$CONNECTION_ID&workflow_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workflow_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docuPandaDocumentUnderstanding/latest/actions/delete-workflow?${params}`, {
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
| `workflow_id` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean | Whether the deletion was successful or not. |

## Native endpoint

Through the native DocuPanda - Document Understanding API, this operation is `DELETE /workflow/:workflow_id` (base URL `https://app.docupipe.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-workflow.md) for the provider-specific parameters and requirements.

