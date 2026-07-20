# E2B Universal API Examples

These examples use the MindCloud API key and E2B connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Sandboxes

Retrieves a list of running sandboxes from E2B.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/e2B/latest/actions/list-sandboxes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/e2B/latest/actions/list-sandboxes?${params}`, {
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
      "alias": "string",
      "clientID": "string",
      "cpuCount": 1,
      "diskSizeMB": 1,
      "endAt": "2026-05-07T12:00:00.000Z",
      "envdVersion": "string",
      "memoryMB": 1,
      "metadata": {},
      "sandboxID": "string",
      "startedAt": "2026-05-07T12:00:00.000Z",
      "state": "string",
      "templateID": "string",
      "volumeMounts": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Sandboxes action reference](actions/list-sandboxes.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/e2B/latest/actions/list-sandboxes).

## Assign Tags

Assigns tags to a template build in E2B.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/e2B/latest/actions/assign-tags" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "tags[]": [
    "string"
  ],
  "target": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/e2B/latest/actions/assign-tags', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "tags[]": ["string"],
    "target": "string"
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
      "buildID": "string",
      "tags": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

See the full [Assign Tags action reference](actions/assign-tags.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/e2B/latest/actions/assign-tags).
