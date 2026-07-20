# folk Universal API Examples

These examples use the MindCloud API key and folk connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List People

Retrieves a list of people from folk.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/folk/latest/actions/list-people?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/folk/latest/actions/list-people?${params}`, {
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
      "addresses": [
        "string"
      ],
      "birthday": "2026-05-07T12:00:00.000Z",
      "companies": [
        {}
      ],
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdBy": {},
      "customFieldValues": {},
      "description": "string",
      "emails": [
        "ava@example.com"
      ],
      "firstName": "Ava",
      "fullName": "Ava Chen",
      "groups": [
        {}
      ],
      "id": "string",
      "interactionMetadata": {},
      "jobTitle": "string",
      "lastName": "Chen",
      "phones": [
        "string"
      ],
      "strongestConnection": {},
      "urls": [
        "https://example.com"
      ]
    }
  ],
  "meta": {}
}
```

See the full [List People action reference](actions/list-people.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/folk/latest/actions/list-people).

## Create Company

Creates a new company in folk.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/folk/latest/actions/create-company" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/folk/latest/actions/create-company', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
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
      "addresses": [
        "string"
      ],
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdBy": {},
      "customFieldValues": {},
      "description": "string",
      "emails": [
        "ava@example.com"
      ],
      "employeeRange": "string",
      "foundationYear": 1,
      "fundingRaised": 1,
      "groups": [
        {}
      ],
      "id": "string",
      "industry": "string",
      "lastFundingDate": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "phones": [
        "string"
      ],
      "urls": [
        "https://example.com"
      ]
    }
  ],
  "meta": {}
}
```

See the full [Create Company action reference](actions/create-company.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/folk/latest/actions/create-company).
