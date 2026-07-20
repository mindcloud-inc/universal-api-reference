# Voog Universal API Examples

These examples use the MindCloud API key and Voog connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List My Sites

Retrieves all available sites from your Voog account.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/voog/latest/actions/list-my-sites?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/voog/latest/actions/list-my-sites?${params}`, {
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

See the full [List My Sites action reference](actions/list-my-sites.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/voog/latest/actions/list-my-sites).

## Confirm Asset Upload

Confirms an asset upload in the current Voog site.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/voog/latest/actions/confirm-asset-upload" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "assetId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/voog/latest/actions/confirm-asset-upload', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "assetId": 1
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

See the full [Confirm Asset Upload action reference](actions/confirm-asset-upload.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/voog/latest/actions/confirm-asset-upload).
