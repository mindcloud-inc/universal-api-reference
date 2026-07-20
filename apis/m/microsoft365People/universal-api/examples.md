# Microsoft 365 People Universal API Examples

These examples use the MindCloud API key and Microsoft 365 People connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List People

Retrieves relevant people from Microsoft 365 People.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoft365People/latest/actions/list-people?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/microsoft365People/latest/actions/list-people?${params}`, {
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
      "companyName": "Ava Chen",
      "department": "string",
      "displayName": "Ava Chen",
      "givenName": "Ava",
      "id": "string",
      "jobTitle": "string",
      "officeLocation": "string",
      "personType": {
        "class": "string",
        "subclass": "string"
      },
      "phones": [
        {
          "number": "string",
          "type": "string"
        }
      ],
      "scoredEmailAddresses": [
        {
          "address": "ava@example.com",
          "relevanceScore": 1
        }
      ],
      "surname": "Chen"
    }
  ],
  "meta": {}
}
```

See the full [List People action reference](actions/list-people.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/microsoft365People/latest/actions/list-people).

## Create Contact

Creates a new contact in Microsoft 365 People.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/microsoft365People/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "displayName": "Jamie Royce"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/microsoft365People/latest/actions/create-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "displayName": "Jamie Royce"
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
      "companyName": "Ava Chen",
      "displayName": "Ava Chen",
      "emailAddresses": [
        {
          "address": "ava@example.com",
          "name": "ava@example.com"
        }
      ],
      "givenName": "Ava Chen",
      "id": "string",
      "jobTitle": "string",
      "mobilePhone": "string",
      "surname": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Create Contact action reference](actions/create-contact.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/microsoft365People/latest/actions/create-contact).
