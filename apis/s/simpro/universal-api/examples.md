# Simpro Universal API Examples

These examples use the MindCloud API key and Simpro connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Companies



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/simpro/latest/actions/list-companies?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/simpro/latest/actions/list-companies?${params}`, {
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
      "id": 1,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [List Companies action reference](actions/list-companies.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/simpro/latest/actions/list-companies).

## Create Contact



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/simpro/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "companyId": "0",
  "GivenName": "Morgan"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/simpro/latest/actions/create-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "companyId": "0",
    "GivenName": "Morgan"
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
      "altPhone": "string",
      "cellPhone": "string",
      "dateModified": "string",
      "department": "string",
      "email": "ava@example.com",
      "familyName": "Ava Chen",
      "fax": "string",
      "givenName": "Ava Chen",
      "id": 1,
      "notes": "string",
      "position": "string",
      "title": "string",
      "workPhone": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Contact action reference](actions/create-contact.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/simpro/latest/actions/create-contact).
