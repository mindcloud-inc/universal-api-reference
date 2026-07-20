# Global Patron Universal API Examples

These examples use the MindCloud API key and Global Patron connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Accessible Forms

Lists accessible forms in Global Patron.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/globalPatron/latest/actions/list-accessible-forms?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/globalPatron/latest/actions/list-accessible-forms?${params}`, {
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
      "accessibleFormIdsAccountManagementAccess": [
        "string"
      ],
      "accessibleFormIdsEditAccess": [
        "string"
      ],
      "accessibleFormIdsFullReportingAccess": [
        "string"
      ],
      "results": [
        {
          "createdDateUtc": "2026-05-07T12:00:00.000Z",
          "formConfiguration": {
            "settings": {
              "formDescription": "string",
              "formName": "Ava Chen",
              "formSystemVersion": 1,
              "formType": "string"
            }
          },
          "id": "string",
          "modifiedDateUtc": "2026-05-07T12:00:00.000Z"
        }
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Accessible Forms action reference](actions/list-accessible-forms.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/globalPatron/latest/actions/list-accessible-forms).

## Add Form Submission Webhook

Adds a form submission webhook in Global Patron.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/globalPatron/latest/actions/add-form-submission-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "formId": "string",
  "webhookUrl": "https://example.com",
  "webhookName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/globalPatron/latest/actions/add-form-submission-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "formId": "string",
    "webhookUrl": "https://example.com",
    "webhookName": "Ava Chen"
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
      "actionSuccessful": true,
      "error": "string",
      "formId": "string",
      "id": "string",
      "message": "string",
      "webhookDestinationUrl": "https://example.com",
      "webhookName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Add Form Submission Webhook action reference](actions/add-form-submission-webhook.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/globalPatron/latest/actions/add-form-submission-webhook).
