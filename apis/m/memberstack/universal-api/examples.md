# Memberstack Universal API Examples

These examples use the MindCloud API key and Memberstack connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Data Tables



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/memberstack/latest/actions/list-data-tables?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/memberstack/latest/actions/list-data-tables?${params}`, {
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
      "tables": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Data Tables action reference](actions/list-data-tables.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/memberstack/latest/actions/list-data-tables).

## Add Free Plan to Member



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/memberstack/latest/actions/add-free-plan-to-member" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "planId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/memberstack/latest/actions/add-free-plan-to-member', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "planId": "string"
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
      "auth": {},
      "createdAt": "2026-05-07T12:00:00.000Z",
      "customFields": {},
      "id": "string",
      "lastLogin": "2026-05-07T12:00:00.000Z",
      "loginRedirect": "string",
      "metaData": {},
      "permissions": [
        "string"
      ],
      "planConnections": [
        {}
      ],
      "profileImage": "string",
      "stripeCustomerId": "string",
      "verified": true
    }
  ],
  "meta": {}
}
```

See the full [Add Free Plan to Member action reference](actions/add-free-plan-to-member.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/memberstack/latest/actions/add-free-plan-to-member).
