# Simplicate Universal API Examples

These examples use the MindCloud API key and Simplicate connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Organizations



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/simplicate/latest/actions/list-organizations?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/simplicate/latest/actions/list-organizations?${params}`, {
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
      "allowAutocollect": "string",
      "cocCode": "string",
      "created": "string",
      "createdAt": "string",
      "debtor": {
        "attentionTo": "string",
        "autocollect": true,
        "autosendSubscriptionInvoice": true,
        "paymentTerm": {
          "days": 1,
          "id": "string",
          "method": "string",
          "name": "Ava Chen"
        },
        "provisionMethod": "string",
        "sendEmailType": "ava@example.com",
        "sendInvoiceEmailToCc": true,
        "sendInvoiceEmailToContact": true,
        "sendInvoiceEmailToFixedEmail": true,
        "sendInvoiceEmailToProjectContact": true
      },
      "email": "ava@example.com",
      "hasDifferentPostalAddress": true,
      "id": "string",
      "industry": {
        "id": "string",
        "name": "Ava Chen"
      },
      "isActive": true,
      "linkedinUrl": "https://example.com",
      "linkedPersonsContacts": [
        {
          "familyName": "https://example.com",
          "familyNamePrefix": "https://example.com",
          "firstName": "https://example.com",
          "id": "https://example.com",
          "isActive": true,
          "personId": "https://example.com",
          "workEmail": "ava@example.com",
          "workFunction": "https://example.com",
          "workMobile": "https://example.com"
        }
      ],
      "modified": "string",
      "name": "Ava Chen",
      "note": "string",
      "phone": "string",
      "relationManager": {
        "id": "string",
        "name": "Ava Chen"
      },
      "relationType": {
        "color": "string",
        "id": "string",
        "label": "string"
      },
      "simplicateUrl": "https://example.com",
      "timelineEmailAddress": "ava@example.com",
      "updatedAt": "string",
      "url": "https://example.com",
      "visitingAddress": {
        "country": "string",
        "countryCode": "string",
        "countryId": "string",
        "id": "string",
        "line1": "string",
        "locality": "string",
        "postalCode": "string",
        "type": "string"
      }
    }
  ],
  "meta": {}
}
```

See the full [List Organizations action reference](actions/list-organizations.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/simplicate/latest/actions/list-organizations).

## Create Employee



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/simplicate/latest/actions/create-employee" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "personId": "string",
  "supervisor": {},
  "status": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/simplicate/latest/actions/create-employee', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "personId": "string",
    "supervisor": {},
    "status": {}
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
      "id": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Employee action reference](actions/create-employee.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/simplicate/latest/actions/create-employee).
