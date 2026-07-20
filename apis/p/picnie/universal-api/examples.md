# Picnie Universal API Examples

These examples use the MindCloud API key and Picnie connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Template

Retrieves a template and its fields from Picnie.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/picnie/latest/actions/get-template?connectionId=$CONNECTION_ID&templateId=2075" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "templateId": "2075"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/picnie/latest/actions/get-template?${params}`, {
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
      "completeObject": {
        "details": [
          {
            "imageUrl": "https://example.com",
            "name": "Ava Chen"
          }
        ],
        "name": "Ava Chen",
        "type": "string"
      },
      "error": true,
      "message": "string",
      "userObject": {
        "details": [
          {
            "imageUrl": "https://example.com",
            "name": "Ava Chen"
          }
        ],
        "templateId": 1,
        "templateName": "Ava Chen",
        "type": "string"
      }
    }
  ],
  "meta": {}
}
```

See the full [Get Template action reference](actions/get-template.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/picnie/latest/actions/get-template).

## Add Image Watermark

Creates a watermarked image in Picnie using an image.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/picnie/latest/actions/add-image-watermark" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": 1,
  "backgroundImageUrl": "https://example.com",
  "frontImageUrl": "https://example.com",
  "position": "br",
  "imageMaxWidth": "800",
  "imageMaxHeight": "800"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/picnie/latest/actions/add-image-watermark', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": 1,
    "backgroundImageUrl": "https://example.com",
    "frontImageUrl": "https://example.com",
    "position": "br",
    "imageMaxWidth": "800",
    "imageMaxHeight": "800"
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
      "error": true,
      "message": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Add Image Watermark action reference](actions/add-image-watermark.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/picnie/latest/actions/add-image-watermark).
