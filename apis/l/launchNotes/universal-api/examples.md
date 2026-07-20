# LaunchNotes Universal API Examples

These examples use the MindCloud API key and LaunchNotes connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Viewer



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/launchNotes/latest/actions/get-viewer?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/launchNotes/latest/actions/get-viewer?${params}`, {
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "id": "string",
      "name": "Ava Chen",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [Get Viewer action reference](actions/get-viewer.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/launchNotes/latest/actions/get-viewer).

## Archive Announcement



```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/launchNotes/latest/actions/archive-announcement" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "input": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/launchNotes/latest/actions/archive-announcement', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "input": {}
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
      "announcement": {},
      "clientMutationId": "string",
      "errors": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [Archive Announcement action reference](actions/archive-announcement.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/launchNotes/latest/actions/archive-announcement).
