# Mux Universal API Examples

These examples use the MindCloud API key and Mux connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Assets



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mux/latest/actions/list-assets?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mux/latest/actions/list-assets?${params}`, {
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
      "nextCursor": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Assets action reference](actions/list-assets.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/mux/latest/actions/list-assets).

## Cancel Direct Upload



```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/mux/latest/actions/cancel-direct-upload" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "uploadId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mux/latest/actions/cancel-direct-upload', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "uploadId": "string"
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
      "data": {}
    }
  ],
  "meta": {}
}
```

See the full [Cancel Direct Upload action reference](actions/cancel-direct-upload.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/mux/latest/actions/cancel-direct-upload).
