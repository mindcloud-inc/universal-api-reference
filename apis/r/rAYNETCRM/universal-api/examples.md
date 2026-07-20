# RAYNET CRM Universal API Examples

These examples use the MindCloud API key and RAYNET CRM connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Contacts



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rAYNETCRM/latest/actions/list-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rAYNETCRM/latest/actions/list-contacts?${params}`, {
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
      "activeUserAccount": true,
      "companyAddress": {
        "address": {
          "country": "string",
          "countryCode": "string"
        }
      },
      "contactInfo": {
        "email": "ava@example.com",
        "email2": "ava@example.com",
        "tel1": "string"
      },
      "firstName": "Ava",
      "id": 1,
      "keyman": true,
      "lastName": "Chen",
      "owner": {
        "fullName": "Ava Chen"
      },
      "primaryRelationship": {
        "company": {
          "id": 1,
          "name": "Ava Chen"
        },
        "type": "string"
      },
      "rowInfo": {
        "createdAt": "2026-05-07T12:00:00.000Z"
      }
    }
  ],
  "meta": {}
}
```

See the full [List Contacts action reference](actions/list-contacts.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/rAYNETCRM/latest/actions/list-contacts).

## Convert Lead



```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/rAYNETCRM/latest/actions/convert-lead" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "leadId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rAYNETCRM/latest/actions/convert-lead', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "leadId": "string"
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
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Convert Lead action reference](actions/convert-lead.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/rAYNETCRM/latest/actions/convert-lead).
