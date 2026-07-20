# Clicksign: Update Document

Updates an existing document in Clicksign.

```
PUT https://connect.mindcloud.co/v1/universal/clicksign/latest/actions/update-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clicksign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/clicksign/latest/actions/update-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "data.attributes.status": "string",
  "data.id": "string",
  "documentId": "string",
  "envelopeId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clicksign/latest/actions/update-document', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "data.attributes.status": "string",
    "data.id": "string",
    "documentId": "string",
    "envelopeId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `data` | object | no | JSON:API document wrapper. |
| `data.attributes` | object | no | Document attributes. |
| `data.attributes.status` | string | yes | The document status. |
| `data.id` | string | yes | The UUID of the document in the JSON:API body. |
| `documentId` | string | yes | The UUID of the document. |
| `envelopeId` | string | yes | The UUID of the envelope. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Clicksign API returns.

## Native endpoint

Through the native Clicksign API, this operation is `PATCH /envelopes/:envelope_id/documents/:document_id` (base URL `https://app.clicksign.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-document.md) for the provider-specific parameters and requirements.

