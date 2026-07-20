# Linkbreakers Universal API Examples

These examples use the MindCloud API key and Linkbreakers connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Links

Retrieves a list of links from Linkbreakers.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/linkbreakers/latest/actions/list-links?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/linkbreakers/latest/actions/list-links?${params}`, {
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
      "links": [
        {
          "createdAt": "https://example.com",
          "destination": "https://example.com",
          "directoryId": "https://example.com",
          "entrypoint": "https://example.com",
          "eventCount": 1,
          "id": "https://example.com",
          "metadata": {},
          "name": "https://example.com",
          "shortlink": "https://example.com",
          "updatedAt": "https://example.com",
          "workspaceId": "https://example.com"
        }
      ],
      "nextPageToken": "string",
      "totalCount": 1
    }
  ],
  "meta": {}
}
```

See the full [List Links action reference](actions/list-links.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/linkbreakers/latest/actions/list-links).

## Create a Directory

Creates a new directory in Linkbreakers.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/linkbreakers/latest/actions/create-directory" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/linkbreakers/latest/actions/create-directory', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
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
      "directory": {
        "createdAt": "string",
        "id": "string",
        "name": "Ava Chen",
        "parentDirectoryId": "string",
        "path": "string",
        "updatedAt": "string",
        "workspaceId": "string"
      }
    }
  ],
  "meta": {}
}
```

See the full [Create a Directory action reference](actions/create-directory.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/linkbreakers/latest/actions/create-directory).
