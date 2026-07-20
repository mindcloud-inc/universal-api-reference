# Paperless Universal API Examples

These examples use the MindCloud API key and Paperless connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Templates



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/paperless/latest/actions/list-templates?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/paperless/latest/actions/list-templates?${params}`, {
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
      "count": 1,
      "data": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Templates action reference](actions/list-templates.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/paperless/latest/actions/list-templates).

## Create Advanced Document



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/paperless/latest/actions/create-advanced-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workspaceId": 1,
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/paperless/latest/actions/create-advanced-document', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workspaceId": 1,
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
      "created_at": "string",
      "id": 1,
      "name": "Ava Chen",
      "status": "string",
      "updated_at": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Advanced Document action reference](actions/create-advanced-document.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/paperless/latest/actions/create-advanced-document).
