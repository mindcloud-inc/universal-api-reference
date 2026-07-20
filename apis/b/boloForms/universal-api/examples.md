# BoloForms Universal API Examples

These examples use the MindCloud API key and BoloForms connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Documents

Retrieves documents from BoloForms.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/boloForms/latest/actions/list-documents?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/boloForms/latest/actions/list-documents?${params}`, {
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
      "authorEmail": "ava@example.com",
      "createdAt": "string",
      "createdBy": {},
      "documentId": "string",
      "documentName": "Ava Chen",
      "documentUrl": "https://example.com",
      "history": [
        {}
      ],
      "Id": "string",
      "isAllSigned": true,
      "isArchived": true,
      "isSigningOrderData": true,
      "metafields": {},
      "pagesCount": 1,
      "respondentsOfDoc": [
        {}
      ],
      "roles": [
        {}
      ],
      "schemaFieldsCount": 1,
      "sentViaSMS": true,
      "settings": {},
      "signType": "string",
      "status": "string",
      "totalRespondants": 1,
      "totalSignedRespondants": 1,
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Documents action reference](actions/list-documents.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/boloForms/latest/actions/list-documents).

## Send Template For Signing

Sends a BoloForms template for signing.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/boloForms/latest/actions/send-template-for-signing" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "documentId": "string",
  "signingType": "0",
  "receiversList[]": [
    {}
  ],
  "receiversList[].name": "Ava Chen",
  "receiversList[].email": "ava@example.com",
  "customVariables[].varName": "Ava Chen",
  "customVariables[].varValue": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/boloForms/latest/actions/send-template-for-signing', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "documentId": "string",
    "signingType": "0",
    "receiversList[]": [{}],
    "receiversList[].name": "Ava Chen",
    "receiversList[].email": "ava@example.com",
    "customVariables[].varName": "Ava Chen",
    "customVariables[].varValue": "string"
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
      "createdDocumentId": "string",
      "createdDocumentStatus": "string",
      "message": "string",
      "signers": [
        {}
      ],
      "templateId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Send Template For Signing action reference](actions/send-template-for-signing.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/boloForms/latest/actions/send-template-for-signing).
