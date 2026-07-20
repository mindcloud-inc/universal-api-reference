# Mailchimp Universal API Examples

These examples use the MindCloud API key and Mailchimp connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Audiences

Retrieves audiences from Mailchimp.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailChimp/latest/actions/list-audiences?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailChimp/latest/actions/list-audiences?${params}`, {
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
      "constraints": {
        "currentTotalInstances": 1,
        "maxInstances": 1,
        "mayCreate": true
      },
      "links": [
        [
          {}
        ]
      ],
      "lists": [
        [
          {}
        ]
      ],
      "totalItems": 1
    }
  ],
  "meta": {}
}
```

See the full [List Audiences action reference](actions/list-audiences.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/mailChimp/latest/actions/list-audiences).

## Add Audience

Creates a new audience in Mailchimp.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mailChimp/latest/actions/add-audience" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "permission_reminder": "string",
  "email_type_option": true,
  "contact": {},
  "campaign_defaults": {},
  "contact.company": "string",
  "contact.address1": "string",
  "contact.city": "string",
  "contact.country": "string",
  "campaign_defaults.from_name": "Ava Chen",
  "campaign_defaults.from_email": "ava@example.com",
  "campaign_defaults.subject": "string",
  "campaign_defaults.language": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mailChimp/latest/actions/add-audience', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "permission_reminder": "string",
    "email_type_option": true,
    "contact": {},
    "campaign_defaults": {},
    "contact.company": "string",
    "contact.address1": "string",
    "contact.city": "string",
    "contact.country": "string",
    "campaign_defaults.from_name": "Ava Chen",
    "campaign_defaults.from_email": "ava@example.com",
    "campaign_defaults.subject": "string",
    "campaign_defaults.language": "string"
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
      "campaignDefaults": {},
      "contact": {},
      "dateCreated": "2026-05-07T12:00:00.000Z",
      "emailTypeOption": true,
      "id": "string",
      "name": "Ava Chen",
      "permissionReminder": "string",
      "webId": 1
    }
  ],
  "meta": {}
}
```

See the full [Add Audience action reference](actions/add-audience.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/mailChimp/latest/actions/add-audience).
