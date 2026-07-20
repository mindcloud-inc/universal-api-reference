# PixelBin.io Universal API Examples

These examples use the MindCloud API key and PixelBin.io connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Files

Retrieves files and folders from PixelBin.io storage.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pixelBinio/latest/actions/list-files?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pixelBinio/latest/actions/list-files?${params}`, {
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
      "_id": "string",
      "access": "string",
      "fileId": "string",
      "format": "string",
      "name": "Ava Chen",
      "path": "string",
      "size": 1,
      "type": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [List Files action reference](actions/list-files.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pixelBinio/latest/actions/list-files).

## Add Transformation Module Credentials

Creates new transformation module credentials in PixelBin.io.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pixelBinio/latest/actions/add-credentials" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "credentials": {},
  "pluginId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pixelBinio/latest/actions/add-credentials', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "credentials": {},
    "pluginId": "string"
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
      "credentials": {}
    }
  ],
  "meta": {}
}
```

See the full [Add Transformation Module Credentials action reference](actions/add-credentials.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pixelBinio/latest/actions/add-credentials).
