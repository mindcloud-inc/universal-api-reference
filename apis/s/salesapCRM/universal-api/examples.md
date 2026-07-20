# SalesapCRM Universal API Examples

These examples use the MindCloud API key and SalesapCRM connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current Token

Retrieves the current token details from SalesapCRM.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/salesapCRM/latest/actions/get-current-token?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/salesapCRM/latest/actions/get-current-token?${params}`, {
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
      "attributes": {
        "created-at": "2026-05-07T12:00:00.000Z",
        "options": {},
        "scopes": [
          "string"
        ],
        "token": "string",
        "updated-at": "2026-05-07T12:00:00.000Z",
        "user-id": 1
      },
      "id": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Current Token action reference](actions/get-current-token.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/salesapCRM/latest/actions/get-current-token).

## Create Company

Creates a company in SalesapCRM.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/salesapCRM/latest/actions/create-company" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "data": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/salesapCRM/latest/actions/create-company', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "data": {}
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
      "attributes": {},
      "id": "string",
      "links": {},
      "relationships": {},
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Company action reference](actions/create-company.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/salesapCRM/latest/actions/create-company).
