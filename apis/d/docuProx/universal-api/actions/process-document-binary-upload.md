# DocuProx: Process Document Binary Upload



```
POST https://connect.mindcloud.co/v1/universal/docuProx/latest/actions/process-document-binary-upload
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocuProx `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/docuProx/latest/actions/process-document-binary-upload" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "templateId": "string",
  "documentFile": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/docuProx/latest/actions/process-document-binary-upload', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "templateId": "string",
    "documentFile": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `templateId` | string | yes | UUID of the DocuProx template to use. |
| `documentFile` | file | yes | Binary document stream uploaded as the raw request body. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native DocuProx API returns.

## Native endpoint

Through the native DocuProx API, this operation is `PUT /v1/process` (base URL `https://api.docuprox.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/process-document-binary-upload.md) for the provider-specific parameters and requirements.

