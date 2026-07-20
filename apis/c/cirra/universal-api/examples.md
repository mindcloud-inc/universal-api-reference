# Cirra Universal API Examples

These examples use the MindCloud API key and Cirra connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Threads

Retrieves Cirra threads for the authenticated user.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cirra/latest/actions/list-threads?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cirra/latest/actions/list-threads?${params}`, {
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
      "archivedAt": "2026-05-07T12:00:00.000Z",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "projectId": "string",
      "status": "string",
      "title": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [List Threads action reference](actions/list-threads.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/cirra/latest/actions/list-threads).

## Archive Thread

Archives an existing Cirra thread by thread ID.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/cirra/latest/actions/archive-thread" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "threadId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cirra/latest/actions/archive-thread', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "threadId": "string"
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
      "archivedAt": "2026-05-07T12:00:00.000Z",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "projectId": "string",
      "status": "string",
      "title": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [Archive Thread action reference](actions/archive-thread.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/cirra/latest/actions/archive-thread).
