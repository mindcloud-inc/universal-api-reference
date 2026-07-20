# Morgen Universal API Examples

These examples use the MindCloud API key and Morgen connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Integration Accounts

Retrieves connected integration accounts from Morgen.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/morgen/latest/actions/list-integration-accounts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/morgen/latest/actions/list-integration-accounts?${params}`, {
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

See the full [List Integration Accounts action reference](actions/list-integration-accounts.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/morgen/latest/actions/list-integration-accounts).

## Close Task

Marks a task as completed in Morgen.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/morgen/latest/actions/close-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/morgen/latest/actions/close-task', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
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

See the full [Close Task action reference](actions/close-task.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/morgen/latest/actions/close-task).
