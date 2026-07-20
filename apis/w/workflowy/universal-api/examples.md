# Workflowy Universal API Examples

These examples use the MindCloud API key and Workflowy connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Targets

Retrieves available targets from the Workflowy account.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/workflowy/latest/actions/list-targets?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/workflowy/latest/actions/list-targets?${params}`, {
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
      "key": "string",
      "name": "Ava Chen",
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Targets action reference](actions/list-targets.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/workflowy/latest/actions/list-targets).

## Complete Node

Marks a Workflowy node as completed.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/workflowy/latest/actions/complete-node" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/workflowy/latest/actions/complete-node', {
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
  "data": [
    {
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Complete Node action reference](actions/complete-node.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/workflowy/latest/actions/complete-node).
