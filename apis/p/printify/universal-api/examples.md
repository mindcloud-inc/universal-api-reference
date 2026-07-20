# Printify Universal API Examples

These examples use the MindCloud API key and Printify connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Shops

Retrieves shops from Printify.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/printify/latest/actions/list-shops?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/printify/latest/actions/list-shops?${params}`, {
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
      "id": 1,
      "salesChannel": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Shops action reference](actions/list-shops.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/printify/latest/actions/list-shops).

## Archive Upload

Archives an uploaded image in Printify.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/printify/latest/actions/archive-upload" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "image_id": "69d963664abf53269b1252a5"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/printify/latest/actions/archive-upload', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "image_id": "69d963664abf53269b1252a5"
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
      "id": "string"
    }
  ],
  "meta": {}
}
```

See the full [Archive Upload action reference](actions/archive-upload.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/printify/latest/actions/archive-upload).
