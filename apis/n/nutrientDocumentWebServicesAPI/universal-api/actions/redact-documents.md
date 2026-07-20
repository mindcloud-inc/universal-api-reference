# Nutrient Document Web Services: Redact Documents

Updates a document with redactions in Nutrient Document Web Services API.

```
PUT https://connect.mindcloud.co/v1/universal/nutrientDocumentWebServicesAPI/latest/actions/redact-documents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nutrient Document Web Services `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/nutrientDocumentWebServicesAPI/latest/actions/redact-documents" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "strategy": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/nutrientDocumentWebServicesAPI/latest/actions/redact-documents', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "strategy": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `url` | string | no | Public PDF URL to redact. |
| `file` | file | no | PDF file to redact. |
| `strategy` | string | yes | Redaction strategy to apply. |
| `strategyOptions` | object | no | Strategy-specific configuration. |
| `redactionState` | string | no | Whether to stage or apply the redactions. |
| `content[]` | array<object> | no | Specific content targets to redact. |
| `password` | string | no | Password for protected PDF files. |
| `data` | object | no | Multipart request metadata. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Nutrient Document Web Services API returns.

## Native endpoint

Through the native Nutrient Document Web Services API, this operation is `POST /processor/redact` (base URL `https://api.nutrient.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/redact-documents.md) for the provider-specific parameters and requirements.

