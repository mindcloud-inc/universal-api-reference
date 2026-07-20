# Anabix CRM Universal API Examples

These examples use the MindCloud API key and Anabix CRM connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Contacts

Retrieves contact records from Anabix CRM.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/anabixCRM/latest/actions/list-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/anabixCRM/latest/actions/list-contacts?${params}`, {
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
      "customFields": [
        {}
      ],
      "description": "string",
      "email": "ava@example.com",
      "email2": "ava@example.com",
      "email3": "ava@example.com",
      "firstName": "Ava",
      "gdpr": {},
      "idContact": 1,
      "idOrganization": 1,
      "idOwner": 1,
      "lastName": "Chen",
      "lists": [
        {}
      ],
      "organization": "string",
      "phoneNumber": "string",
      "phoneNumber2": "string",
      "phoneNumber3": "string",
      "position": "string",
      "primaryContact": 1,
      "revisionInfo": {},
      "salutation": "string",
      "sex": "string",
      "shippingCity": "string",
      "shippingCode": "string",
      "shippingCountry": "string",
      "shippingStreet": "string",
      "source": "string",
      "title": "Ava Chen",
      "vip": 1,
      "website": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [List Contacts action reference](actions/list-contacts.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/anabixCRM/latest/actions/list-contacts).

## Create Activity

Creates a new activity in Anabix CRM.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/anabixCRM/latest/actions/create-activity" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "data.body": "string",
  "data.idContact": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/anabixCRM/latest/actions/create-activity', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "data.body": "string",
    "data.idContact": 1
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
      "body": "string",
      "customFields": [
        {}
      ],
      "duration": "string",
      "idActivity": 1,
      "idContact": 1,
      "idDeal": 1,
      "revisionInfo": {},
      "timestamp": 1,
      "title": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Activity action reference](actions/create-activity.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/anabixCRM/latest/actions/create-activity).
