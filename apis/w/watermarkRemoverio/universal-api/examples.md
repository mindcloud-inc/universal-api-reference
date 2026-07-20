# WatermarkRemover.io Universal API Examples

These examples use the MindCloud API key and WatermarkRemover.io connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Check Object Size

Checks object size in a file with WatermarkRemover.io.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/watermarkRemoverio/latest/actions/check-object-size?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/watermarkRemoverio/latest/actions/check-object-size?${params}`, {
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
        1
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [Check Object Size action reference](actions/check-object-size.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/watermarkRemoverio/latest/actions/check-object-size).

## Upload Image From URL

Uploads an image to WatermarkRemover.io from a URL.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/watermarkRemoverio/latest/actions/upload-image-from-url" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/watermarkRemoverio/latest/actions/upload-image-from-url', {
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
  "data": [],
  "meta": {}
}
```

See the full [Upload Image From URL action reference](actions/upload-image-from-url.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/watermarkRemoverio/latest/actions/upload-image-from-url).
