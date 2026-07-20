# Zoho Sheet Universal API Examples

These examples use the MindCloud API key and Zoho Sheet connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List All Workbooks

Retrieves all workbooks from Zoho Sheet.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoSheet/latest/actions/list-all-workbooks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoSheet/latest/actions/list-all-workbooks?${params}`, {
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
      "method": "string",
      "resourceCount": 1,
      "resourceEndIndex": 1,
      "resourceStartIndex": 1,
      "status": "string",
      "workbooks": [
        [
          {}
        ]
      ]
    }
  ],
  "meta": {}
}
```

See the full [List All Workbooks action reference](actions/list-all-workbooks.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/zohoSheet/latest/actions/list-all-workbooks).

## Add Records to Table

Adds records to a table in Zoho Sheet.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoSheet/latest/actions/add-records-to-table" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "resourceId": "string",
  "tableName": "Ava Chen",
  "jsonData": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoSheet/latest/actions/add-records-to-table', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "resourceId": "string",
    "tableName": "Ava Chen",
    "jsonData": "string"
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
      "method": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add Records to Table action reference](actions/add-records-to-table.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/zohoSheet/latest/actions/add-records-to-table).
