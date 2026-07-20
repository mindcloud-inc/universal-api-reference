# Digiclose Universal API Examples

These examples use the MindCloud API key and Digiclose connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Contacts



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/digiclose/latest/actions/list-contacts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/digiclose/latest/actions/list-contacts?${params}`, {
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
      "company": "string",
      "email": "ava@example.com",
      "fields": [
        {
          "id": 1,
          "required": true,
          "value": "string"
        }
      ],
      "formatted": "string",
      "id": 1,
      "phone": {},
      "values": {
        "city": {},
        "company": "string",
        "country": {},
        "email": "ava@example.com",
        "firstname": {},
        "lastname": {},
        "phone": {},
        "postcode": {},
        "state": {},
        "street": {}
      }
    }
  ],
  "meta": {}
}
```

See the full [List Contacts action reference](actions/list-contacts.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/digiclose/latest/actions/list-contacts).

## Create Contact



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/digiclose/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fields": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/digiclose/latest/actions/create-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fields": {}
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
      "fields": [
        {
          "id": 1,
          "name": "Ava Chen",
          "value": "string"
        }
      ],
      "id": 1,
      "links": {
        "contact": {
          "href": "https://example.com",
          "type": "https://example.com"
        }
      }
    }
  ],
  "meta": {}
}
```

See the full [Create Contact action reference](actions/create-contact.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/digiclose/latest/actions/create-contact).
