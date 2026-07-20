# PDFMonkey Universal API Examples

These examples use the MindCloud API key and PDFMonkey connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current User

Retrieves the current user from PDFMonkey.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pDFMonkey/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pDFMonkey/latest/actions/get-current-user?${params}`, {
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
      "currentUser": {
        "availableDocuments": 1,
        "blockResources": true,
        "companyName": "Ava Chen",
        "country": "string",
        "createdAt": "2026-05-07T12:00:00.000Z",
        "currentPlan": "string",
        "currentPlanInterval": "string",
        "desiredName": "Ava Chen",
        "email": "ava@example.com",
        "firstName": "Ava",
        "id": "string",
        "lang": "string",
        "lastName": "Chen",
        "onboardingCompletedAt": "2026-05-07T12:00:00.000Z",
        "payingCustomer": true,
        "phoneNumber": "string",
        "shareLinks": true,
        "trialEndsOn": "2026-05-07T12:00:00.000Z",
        "updatedAt": "2026-05-07T12:00:00.000Z",
        "useCase": "string"
      }
    }
  ],
  "meta": {}
}
```

See the full [Get Current User action reference](actions/get-current-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pDFMonkey/latest/actions/get-current-user).

## Create Document

Creates a document asynchronously in PDFMonkey.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pDFMonkey/latest/actions/create-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "documentTemplateId": "12345678-90ab-cdef-1234-567890abcdef"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pDFMonkey/latest/actions/create-document', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "documentTemplateId": "12345678-90ab-cdef-1234-567890abcdef"
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
      "document": {
        "appId": "string",
        "createdAt": "2026-05-07T12:00:00.000Z",
        "documentTemplateId": "string",
        "downloadUrl": "https://example.com",
        "failureCause": "string",
        "filename": "Ava Chen",
        "generationLogs": [
          {}
        ],
        "id": "string",
        "meta": "string",
        "outputType": "string",
        "payload": "string",
        "previewUrl": "https://example.com",
        "publicShareLink": "https://example.com",
        "status": "string",
        "updatedAt": "2026-05-07T12:00:00.000Z",
        "xmlData": "string"
      }
    }
  ],
  "meta": {}
}
```

See the full [Create Document action reference](actions/create-document.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pDFMonkey/latest/actions/create-document).
