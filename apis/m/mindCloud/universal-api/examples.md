# MindCloud Universal API Examples

These examples use the MindCloud API key and MindCloud connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Users



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mindCloud/latest/actions/list-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mindCloud/latest/actions/list-users?${params}`, {
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
  "data": [],
  "meta": {}
}
```

See the full [List Users action reference](actions/list-users.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/mindCloud/latest/actions/list-users).

## Create Company



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mindCloud/latest/actions/create-company" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "ACME Corp."
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mindCloud/latest/actions/create-company', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "ACME Corp."
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
      "data": {
        "createdOn": "string",
        "description": "string",
        "id": "string",
        "isDeleted": {},
        "isPersonal": true,
        "name": "Ava Chen",
        "timezone": {},
        "updatedOn": "string"
      },
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Create Company action reference](actions/create-company.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/mindCloud/latest/actions/create-company).
