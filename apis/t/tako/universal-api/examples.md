# Tako Universal API Examples

These examples use the MindCloud API key and Tako connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Tool Descriptions

Retrieves tool descriptions from Tako.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tako/latest/actions/list-tool-descriptions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tako/latest/actions/list-tool-descriptions?${params}`, {
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
      "search_tools": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Tool Descriptions action reference](actions/list-tool-descriptions.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/tako/latest/actions/list-tool-descriptions).

## Connect File

Connects a file to Tako for analysis.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/tako/latest/actions/connect-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fileUrl": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tako/latest/actions/connect-file', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fileUrl": "https://example.com"
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
      "id": "string",
      "message": "string",
      "metadata": {}
    }
  ],
  "meta": {}
}
```

See the full [Connect File action reference](actions/connect-file.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/tako/latest/actions/connect-file).
