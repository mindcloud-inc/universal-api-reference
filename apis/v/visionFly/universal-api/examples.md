# VisionFly Universal API Examples

These examples use the MindCloud API key and VisionFly connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Test API Key

Retrieves authentication details from VisionFly.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/visionFly/latest/actions/test-api-key?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/visionFly/latest/actions/test-api-key?${params}`, {
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
      "account": {},
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Test API Key action reference](actions/test-api-key.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/visionFly/latest/actions/test-api-key).

## Upload Image to CDN

Uploads an image to the VisionFly CDN.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/visionFly/latest/actions/upload-image-to-cdn" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/visionFly/latest/actions/upload-image-to-cdn', {
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
      "contentType": "string",
      "imageId": "string",
      "size": 1,
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Upload Image to CDN action reference](actions/upload-image-to-cdn.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/visionFly/latest/actions/upload-image-to-cdn).
