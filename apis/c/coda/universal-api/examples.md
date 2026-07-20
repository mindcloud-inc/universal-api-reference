# Coda Universal API Examples

These examples use the MindCloud API key and Coda connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Docs

Retrieves accessible docs from Coda workspaces.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coda/latest/actions/list-docs?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/coda/latest/actions/list-docs?${params}`, {
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
      "browserLink": "https://example.com",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "docSize": {
        "baseTableCount": 1,
        "overApiSizeLimit": true,
        "pageCount": 1,
        "tableAndViewCount": 1,
        "totalRowCount": 1
      },
      "folder": {
        "browserLink": "https://example.com",
        "id": "string",
        "name": "Ava Chen",
        "type": "string"
      },
      "folderId": "string",
      "href": "string",
      "icon": {
        "browserLink": "https://example.com",
        "name": "Ava Chen",
        "type": "string"
      },
      "id": "string",
      "name": "Ava Chen",
      "owner": "string",
      "ownerName": "Ava Chen",
      "sourceDoc": {
        "browserLink": "https://example.com",
        "href": "string",
        "id": "string",
        "type": "string"
      },
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "workspace": {
        "browserLink": "https://example.com",
        "id": "string",
        "name": "Ava Chen",
        "type": "string"
      },
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Docs action reference](actions/list-docs.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/coda/latest/actions/list-docs).

## Create Doc

Creates a new doc in Coda.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/coda/latest/actions/create-doc" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/coda/latest/actions/create-doc', {
  method: 'POST',
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
  "data": [
    {
      "browserLink": "https://example.com",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "folder": {
        "browserLink": "https://example.com",
        "id": "string",
        "name": "Ava Chen",
        "type": "string"
      },
      "folderId": "string",
      "href": "string",
      "icon": {
        "browserLink": "https://example.com",
        "name": "Ava Chen",
        "type": "string"
      },
      "id": "string",
      "name": "Ava Chen",
      "owner": "string",
      "ownerName": "Ava Chen",
      "requestId": "string",
      "sourceDoc": {
        "browserLink": "https://example.com",
        "href": "string",
        "id": "string",
        "type": "string"
      },
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "workspace": {
        "browserLink": "https://example.com",
        "id": "string",
        "name": "Ava Chen",
        "type": "string"
      },
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Doc action reference](actions/create-doc.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/coda/latest/actions/create-doc).
