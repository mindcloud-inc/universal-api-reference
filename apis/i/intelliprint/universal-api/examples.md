# Intelliprint Universal API Examples

These examples use the MindCloud API key and Intelliprint connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Backgrounds



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/intelliprint/latest/actions/list-backgrounds?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/intelliprint/latest/actions/list-backgrounds?${params}`, {
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
      "data": [
        {}
      ],
      "has_more": true,
      "object": "string",
      "total_available": 1
    }
  ],
  "meta": {}
}
```

See the full [List Backgrounds action reference](actions/list-backgrounds.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/intelliprint/latest/actions/list-backgrounds).

## Create Background



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/intelliprint/latest/actions/create-background" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/intelliprint/latest/actions/create-background', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "file": "string"
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
      "account": "string",
      "created": 1,
      "file": {},
      "id": "string",
      "name": "Ava Chen",
      "object": "string",
      "pdf": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Background action reference](actions/create-background.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/intelliprint/latest/actions/create-background).
