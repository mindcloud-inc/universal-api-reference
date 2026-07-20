# Joiin Universal API Examples

These examples use the MindCloud API key and Joiin connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Companies

Retrieves companies from Joiin.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/joiin/latest/actions/list-companies?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/joiin/latest/actions/list-companies?${params}`, {
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
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [List Companies action reference](actions/list-companies.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/joiin/latest/actions/list-companies).

## Create Company

Creates a company in Joiin.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/joiin/latest/actions/create-company" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "sourceSystem": "string",
  "currency": "string",
  "fiscalYearStartMonth": "string",
  "accounts[]": [
    {}
  ],
  "valueFormat": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/joiin/latest/actions/create-company', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "sourceSystem": "string",
    "currency": "string",
    "fiscalYearStartMonth": "string",
    "accounts[]": [{}],
    "valueFormat": "string"
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
      "companyId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Company action reference](actions/create-company.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/joiin/latest/actions/create-company).
