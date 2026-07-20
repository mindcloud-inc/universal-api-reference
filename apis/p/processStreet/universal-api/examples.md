# Process Street Universal API Examples

These examples use the MindCloud API key and Process Street connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Test Authentication



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/processStreet/latest/actions/test-authentication?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/processStreet/latest/actions/test-authentication?${params}`, {
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
      "apiKeyLabel": "string"
    }
  ],
  "meta": {}
}
```

See the full [Test Authentication action reference](actions/test-authentication.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/processStreet/latest/actions/test-authentication).

## Approve or Reject Task



```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/processStreet/latest/actions/approve-or-reject-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workflowRunId": "string",
  "approvalTaskId": "string",
  "status": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/processStreet/latest/actions/approve-or-reject-task', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workflowRunId": "string",
    "approvalTaskId": "string",
    "status": "string"
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

See the full [Approve or Reject Task action reference](actions/approve-or-reject-task.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/processStreet/latest/actions/approve-or-reject-task).
