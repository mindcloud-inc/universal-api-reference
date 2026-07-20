# Nutrient Document Web Services: AI Redact Sensitive Information

Updates a document by redacting sensitive information in Nutrient Document Web Services API.

```
PUT https://connect.mindcloud.co/v1/universal/nutrientDocumentWebServicesAPI/latest/actions/ai-redact-sensitive-information
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nutrient Document Web Services `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/nutrientDocumentWebServicesAPI/latest/actions/ai-redact-sensitive-information" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "documents[]": [
    {}
  ],
  "criteria": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/nutrientDocumentWebServicesAPI/latest/actions/ai-redact-sensitive-information', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "documents[]": [{}],
    "criteria": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `documents[]` | array<object> | yes | Documents to analyze for AI redaction. |
| `criteria` | string | yes | Natural-language redaction criteria. |
| `redactionState` | string | no | Whether to stage or apply the AI redactions. |
| `options` | object | no | Optional AI redaction configuration. |
| `file` | file | no | Document file to redact in multipart requests. |
| `data` | object | no | Multipart request metadata. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Nutrient Document Web Services API returns.

## Native endpoint

Through the native Nutrient Document Web Services API, this operation is `POST /ai/redact` (base URL `https://api.nutrient.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/ai-redact-sensitive-information.md) for the provider-specific parameters and requirements.

