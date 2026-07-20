# PrintNode Universal API Examples

These examples use the MindCloud API key and PrintNode connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Validate Credentials

Validates credentials with PrintNode without performing other actions.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/printNode/latest/actions/validate-credentials?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/printNode/latest/actions/validate-credentials?${params}`, {
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
      "value": "string"
    }
  ],
  "meta": {}
}
```

See the full [Validate Credentials action reference](actions/validate-credentials.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/printNode/latest/actions/validate-credentials).

## Create Print Job

Creates a new print job in PrintNode.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/printNode/latest/actions/create-print-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "printerId": 1,
  "contentType": "string",
  "content": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/printNode/latest/actions/create-print-job', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "printerId": 1,
    "contentType": "string",
    "content": "string"
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
      "value": 1
    }
  ],
  "meta": {}
}
```

See the full [Create Print Job action reference](actions/create-print-job.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/printNode/latest/actions/create-print-job).
