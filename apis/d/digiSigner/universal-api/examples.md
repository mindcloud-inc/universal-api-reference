# DigiSigner Universal API Examples

These examples use the MindCloud API key and DigiSigner connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Document Fields

Retrieves document fields from DigiSigner by document ID.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/digiSigner/latest/actions/get-document-fields?connectionId=$CONNECTION_ID&documentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "documentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/digiSigner/latest/actions/get-document-fields?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "document_fields": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [Get Document Fields action reference](actions/get-document-fields.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/digiSigner/latest/actions/get-document-fields).

## Send Signature Request

Creates a signature request in DigiSigner.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/digiSigner/latest/actions/send-signature-request" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "documents[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/digiSigner/latest/actions/send-signature-request', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "documents[]": [{}]
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "documents": [
        {}
      ],
      "embedded": true,
      "hide_text_tags": true,
      "is_completed": true,
      "send_documents_as_bundle": true,
      "send_emails": true,
      "send_reminder_emails": true,
      "signature_request_id": "string",
      "use_text_tags": true
    }
  ],
  "meta": {}
}
```

See the full [Send Signature Request action reference](actions/send-signature-request.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/digiSigner/latest/actions/send-signature-request).
