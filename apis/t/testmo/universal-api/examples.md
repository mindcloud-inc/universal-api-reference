# Testmo Universal API Examples

These examples use the MindCloud API key and Testmo connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current User

Retrieves the authenticated user from Testmo.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/testmo/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/testmo/latest/actions/get-current-user?${params}`, {
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

See the full [Get Current User action reference](actions/get-current-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/testmo/latest/actions/get-current-user).

## Complete Automation Run

Marks an automation run as completed in Testmo.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/testmo/latest/actions/complete-automation-run" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "automationRunId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/testmo/latest/actions/complete-automation-run', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "automationRunId": 1
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

See the full [Complete Automation Run action reference](actions/complete-automation-run.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/testmo/latest/actions/complete-automation-run).
