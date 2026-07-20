# data.world Universal API Examples

These examples use the MindCloud API key and data.world connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Describe a SQL Query

Describes a SQL query in data.world.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dataworld/latest/actions/describe-sql-query?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dataworld/latest/actions/describe-sql-query?${params}`, {
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
      "fields": [
        {
          "name": "Ava Chen",
          "type": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

See the full [Describe a SQL Query action reference](actions/describe-sql-query.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/dataworld/latest/actions/describe-sql-query).

## Add Files from URLs

Adds files from URLs to a dataset in data.world.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dataworld/latest/actions/add-files-from-urls" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dataworld/latest/actions/add-files-from-urls', {
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
      "file": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add Files from URLs action reference](actions/add-files-from-urls.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/dataworld/latest/actions/add-files-from-urls).
