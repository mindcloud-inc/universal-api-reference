# Memento Database Universal API Examples

These examples use the MindCloud API key and Memento Database connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Libraries

Retrieves all libraries from Memento Database.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mementoDatabase/latest/actions/list-libraries?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mementoDatabase/latest/actions/list-libraries?${params}`, {
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
      "libraries": [
        {}
      ],
      "nextPageToken": "string",
      "revision": 1
    }
  ],
  "meta": {}
}
```

See the full [List Libraries action reference](actions/list-libraries.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/mementoDatabase/latest/actions/list-libraries).

## Create Entry

Creates a new entry in a Memento Database library.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mementoDatabase/latest/actions/create-entry" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "libraryId": "string",
  "fields[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mementoDatabase/latest/actions/create-entry', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "libraryId": "string",
    "fields[]": [{}]
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
      "author": "string",
      "createdTime": "string",
      "fields": [
        {}
      ],
      "id": "string",
      "modifiedTime": "string",
      "revision": 1,
      "size": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Entry action reference](actions/create-entry.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/mementoDatabase/latest/actions/create-entry).
