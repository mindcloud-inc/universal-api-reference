# Xata Universal API Examples

These examples use the MindCloud API key and Xata connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get list of organizations



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xata/latest/actions/get-organizations-list?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xata/latest/actions/get-organizations-list?${params}`, {
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
      "organizations": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [Get list of organizations action reference](actions/get-organizations-list.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/xata/latest/actions/get-organizations-list).

## Retrieve branch logs



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/xata/latest/actions/branch-logs" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "organizationID": "string",
  "projectID": "string",
  "branchID": "string",
  "start": "2026-05-07T12:00:00.000Z",
  "end": "2026-05-07T12:00:00.000Z"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/xata/latest/actions/branch-logs', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "organizationID": "string",
    "projectID": "string",
    "branchID": "string",
    "start": "2026-05-07T12:00:00.000Z",
    "end": "2026-05-07T12:00:00.000Z"
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
      "end": "2026-05-07T12:00:00.000Z",
      "logs": [
        {}
      ],
      "nextCursor": "string",
      "start": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [Retrieve branch logs action reference](actions/branch-logs.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/xata/latest/actions/branch-logs).
