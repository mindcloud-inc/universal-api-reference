# Ragic Universal API Examples

These examples use the MindCloud API key and Ragic connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Records

Retrieves records from Ragic.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ragic/latest/actions/list-records?connectionId=$CONNECTION_ID&limit=25&offset=0&tabFolderPath=ragic-setup&sheetIndex=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "tabFolderPath": "ragic-setup",
  "sheetIndex": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ragic/latest/actions/list-records?${params}`, {
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
  "data": [],
  "meta": {}
}
```

See the full [List Records action reference](actions/list-records.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/ragic/latest/actions/list-records).

## Add Record Comment

Adds a comment to a record in Ragic.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/ragic/latest/actions/add-record-comment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "tabFolderPath": "ragic-setup",
  "sheetIndex": "8",
  "recordId": "0",
  "comment": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ragic/latest/actions/add-record-comment', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "tabFolderPath": "ragic-setup",
    "sheetIndex": "8",
    "recordId": "0",
    "comment": "string"
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

See the full [Add Record Comment action reference](actions/add-record-comment.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/ragic/latest/actions/add-record-comment).
