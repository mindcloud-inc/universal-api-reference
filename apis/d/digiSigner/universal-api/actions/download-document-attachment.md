# DigiSigner: Download Document Attachment

Downloads a document attachment from DigiSigner by field ID.

```
GET https://connect.mindcloud.co/v1/universal/digiSigner/latest/actions/download-document-attachment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DigiSigner `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/digiSigner/latest/actions/download-document-attachment?connectionId=$CONNECTION_ID&documentId=5be88823-3ff5-4ec4-8175-459dee50f7fb&fieldApiId=06e28f74-1464-4890-9825-4ec0df1357c5" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "documentId": "5be88823-3ff5-4ec4-8175-459dee50f7fb",
  "fieldApiId": "06e28f74-1464-4890-9825-4ec0df1357c5"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/digiSigner/latest/actions/download-document-attachment?${params}`, {
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
| `documentId` | string | yes | DigiSigner document_id that contains the filled attachment field. Use a document from Upload Document, a callback payload, or a signature request response. Example: `5be88823-3ff5-4ec4-8175-459dee50f7fb`. |
| `fieldApiId` | string | yes | The api_id of a filled document field where Get Document Fields returns type ATTACHMENT and status FILLED. Example: `06e28f74-1464-4890-9825-4ec0df1357c5`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native DigiSigner API returns.

## Native endpoint

Through the native DigiSigner API, this operation is `GET /documents/:documentId/fields/:fieldApiId/attachment` (base URL `https://api.digisigner.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/download-document-attachment.md) for the provider-specific parameters and requirements.

