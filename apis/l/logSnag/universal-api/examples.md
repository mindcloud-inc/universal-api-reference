# LogSnag Universal API Examples

These examples use the MindCloud API key and LogSnag connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Group User



```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/logSnag/latest/actions/group-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "project": "string",
  "groupId": "string",
  "userId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/logSnag/latest/actions/group-user', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "project": "string",
    "groupId": "string",
    "userId": "string"
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
      "groupId": "string",
      "project": "string",
      "properties": {},
      "userId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Group User action reference](actions/group-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/logSnag/latest/actions/group-user).
