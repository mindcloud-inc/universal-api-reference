# AltTextify Universal API Examples

These examples use the MindCloud API key and AltTextify connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Images

Retrieves all account images from AltTextify.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/altTextify/latest/actions/list-images?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/altTextify/latest/actions/list-images?${params}`, {
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
      "alt_text": [
        "string"
      ],
      "asset_id": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "image_source": "string",
      "tag": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Images action reference](actions/list-images.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/altTextify/latest/actions/list-images).

## Upload Image From URL

Creates a new image in AltTextify from an image URL.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/altTextify/latest/actions/upload-image-from-url" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "image": "string",
  "lang": "en",
  "maxChars": "120"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/altTextify/latest/actions/upload-image-from-url', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "image": "string",
    "lang": "en",
    "maxChars": "120"
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
      "alt_text": "string",
      "asset_id": "string",
      "async": true,
      "created_at": "2026-05-07T12:00:00.000Z",
      "links": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [Upload Image From URL action reference](actions/upload-image-from-url.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/altTextify/latest/actions/upload-image-from-url).
