# Caspio Universal API Examples

These examples use the MindCloud API key and Caspio connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List File Folders

Retrieves all file folders from Caspio.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/caspio/latest/actions/list-file-folders?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/caspio/latest/actions/list-file-folders?${params}`, {
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
      "Pagination": {},
      "Result": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [List File Folders action reference](actions/list-file-folders.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/caspio/latest/actions/list-file-folders).

## Create Table Record

Creates a new table record in Caspio.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/caspio/latest/actions/create-table-record" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "tableName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/caspio/latest/actions/create-table-record', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "tableName": "Ava Chen"
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

See the full [Create Table Record action reference](actions/create-table-record.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/caspio/latest/actions/create-table-record).
