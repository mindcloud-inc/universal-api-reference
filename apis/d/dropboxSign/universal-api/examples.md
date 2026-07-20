# Dropbox Sign Universal API Examples

These examples use the MindCloud API key and Dropbox Sign connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Account

Retrieves your Dropbox Sign account settings.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dropboxSign/latest/actions/get-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dropboxSign/latest/actions/get-account?${params}`, {
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
      "accountId": "string",
      "callbackUrl": {},
      "emailAddress": "ava@example.com",
      "isLocked": true,
      "isPaidHf": true,
      "isPaidHs": true,
      "locale": "string",
      "quotas": {
        "apiSignatureRequestsLeft": 1,
        "documentsLeft": 1,
        "templatesLeft": 1,
        "templatesTotal": 1
      },
      "roleCode": {},
      "settings": {
        "signerAccessCodes": true,
        "smsAuthentication": true,
        "smsDelivery": true
      }
    }
  ],
  "meta": {}
}
```

See the full [Get Account action reference](actions/get-account.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/dropboxSign/latest/actions/get-account).

## Create Template

Creates a template in Dropbox Sign.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dropboxSign/latest/actions/create-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file_urls[]": [
    "https://example.com"
  ],
  "title": "string",
  "signer_roles[].name": "Ava Chen",
  "signer_roles[].order": 1,
  "form_fields_per_document[].document_index": 1,
  "form_fields_per_document[].api_id": "string",
  "form_fields_per_document[].type": "string",
  "form_fields_per_document[].required": true,
  "form_fields_per_document[].signer": "string",
  "form_fields_per_document[].width": 1,
  "form_fields_per_document[].height": 1,
  "form_fields_per_document[].x": 1,
  "form_fields_per_document[].y": 1,
  "form_fields_per_document[].page": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dropboxSign/latest/actions/create-template', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "file_urls[]": ["https://example.com"],
    "title": "string",
    "signer_roles[].name": "Ava Chen",
    "signer_roles[].order": 1,
    "form_fields_per_document[].document_index": 1,
    "form_fields_per_document[].api_id": "string",
    "form_fields_per_document[].type": "string",
    "form_fields_per_document[].required": true,
    "form_fields_per_document[].signer": "string",
    "form_fields_per_document[].width": 1,
    "form_fields_per_document[].height": 1,
    "form_fields_per_document[].x": 1,
    "form_fields_per_document[].y": 1,
    "form_fields_per_document[].page": 1
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
      "template": {
        "templateId": "string"
      },
      "warnings": [
        {
          "warningMsg": "string",
          "warningName": "Ava Chen"
        }
      ]
    }
  ],
  "meta": {}
}
```

See the full [Create Template action reference](actions/create-template.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/dropboxSign/latest/actions/create-template).
