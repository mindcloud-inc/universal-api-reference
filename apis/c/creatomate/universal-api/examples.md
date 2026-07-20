# Creatomate Universal API Examples

These examples use the MindCloud API key and Creatomate connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Render Status

Retrieves a render's status from Creatomate.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/creatomate/latest/actions/get-render-status?connectionId=$CONNECTION_ID&renderId=c4f6d4f1-7a4e-4b67-9f90-3fc76f3c7d0e" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "renderId": "c4f6d4f1-7a4e-4b67-9f90-3fc76f3c7d0e"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/creatomate/latest/actions/get-render-status?${params}`, {
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
      "duration": 1,
      "error_message": "string",
      "file_size": 1,
      "frame_rate": 1,
      "height": 1,
      "id": "string",
      "metadata": "string",
      "modifications": {},
      "output_format": "string",
      "render_scale": 1,
      "snapshot_url": "https://example.com",
      "status": "string",
      "template_id": "string",
      "template_name": "Ava Chen",
      "template_tags": [
        "string"
      ],
      "url": "https://example.com",
      "webhook_url": "https://example.com",
      "width": 1
    }
  ],
  "meta": {}
}
```

See the full [Get Render Status action reference](actions/get-render-status.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/creatomate/latest/actions/get-render-status).

## Concatenate Multiple Videos

Creates a concatenated video render in Creatomate.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/creatomate/latest/actions/concatenate-multiple-videos" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "videoUrls[]": [
    "https://example.com"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/creatomate/latest/actions/concatenate-multiple-videos', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "videoUrls[]": ["https://example.com"]
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
      "id": "string",
      "outputFormat": "string",
      "status": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Concatenate Multiple Videos action reference](actions/concatenate-multiple-videos.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/creatomate/latest/actions/concatenate-multiple-videos).
