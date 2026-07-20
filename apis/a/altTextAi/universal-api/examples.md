# AltText.Ai Universal API Examples

These examples use the MindCloud API key and AltText.Ai connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Images

Retrieves images from your AltText.Ai library.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/altTextAi/latest/actions/list-images?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/altTextAi/latest/actions/list-images?${params}`, {
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
      "altText": "string",
      "altTexts": {},
      "assetId": "string",
      "createdAt": 1,
      "errorCode": "string",
      "errors": {},
      "metadata": {},
      "tags": [
        "string"
      ],
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [List Images action reference](actions/list-images.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/altTextAi/latest/actions/list-images).

## Bulk Upload Images

Bulk uploads image URLs for alt text generation in AltText.Ai.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/altTextAi/latest/actions/bulk-upload-images" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/altTextAi/latest/actions/bulk-upload-images', {
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
      "error": "string",
      "rowErrors": [
        [
          "string"
        ]
      ],
      "rows": 1,
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Bulk Upload Images action reference](actions/bulk-upload-images.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/altTextAi/latest/actions/bulk-upload-images).
