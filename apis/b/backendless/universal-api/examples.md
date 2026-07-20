# Backendless Universal API Examples

These examples use the MindCloud API key and Backendless connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Root Directory

Retrieves the root directory listing from Backendless.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/backendless/latest/actions/list-root-directory?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/backendless/latest/actions/list-root-directory?${params}`, {
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
      "createdOn": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "publicUrl": "https://example.com",
      "updatedOn": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [List Root Directory action reference](actions/list-root-directory.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/backendless/latest/actions/list-root-directory).

## Append File

Appends content to a file in Backendless.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/backendless/latest/actions/append-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/backendless/latest/actions/append-file', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
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

See the full [Append File action reference](actions/append-file.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/backendless/latest/actions/append-file).
