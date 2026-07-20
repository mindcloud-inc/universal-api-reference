# PDFMonkey: Delete Template

Deletes an existing template from PDFMonkey.

```
DELETE https://connect.mindcloud.co/v1/universal/pDFMonkey/latest/actions/delete-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PDFMonkey `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/pDFMonkey/latest/actions/delete-template?connectionId=$CONNECTION_ID&id=3e642963-37eb-43ec-a6f5-71be4514b26b" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "3e642963-37eb-43ec-a6f5-71be4514b26b"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pDFMonkey/latest/actions/delete-template?${params}`, {
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
| `id` | string | yes | ID of the template to delete. Example: `3e642963-37eb-43ec-a6f5-71be4514b26b`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deleted": true,
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deleted` | boolean | Whether the delete request succeeded. |
| `id` | string | Deleted template ID from the request context. |

## Native endpoint

Through the native PDFMonkey API, this operation is `DELETE /document_templates/:id` (base URL `https://api.pdfmonkey.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-template.md) for the provider-specific parameters and requirements.

