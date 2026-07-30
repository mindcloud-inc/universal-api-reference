# ConvertAPI Universal API Examples

These examples use the MindCloud API key and ConvertAPI connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get User Info



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/convertAPI/latest/actions/new-action1?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/convertAPI/latest/actions/new-action1?${params}`, {
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
      "active": true,
      "apiKey": 1,
      "conversionsConsumed": 1,
      "conversionsTotal": 1,
      "email": "ava@example.com",
      "fullName": "Ava Chen",
      "secondsLeft": 1,
      "secret": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get User Info action reference](actions/new-action1.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/convertAPI/latest/actions/new-action1).

## Add Image Watermark to PDF

Adds an image watermark to a PDF with ConvertAPI.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/convertAPI/latest/actions/add-image-watermark-to-pdf" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file": "string",
  "imageFile": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/convertAPI/latest/actions/add-image-watermark-to-pdf', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "file": "string",
    "imageFile": "string"
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
      "fileExt": "string",
      "fileId": "string",
      "fileName": "Ava Chen",
      "fileSize": 1,
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Add Image Watermark to PDF action reference](actions/add-image-watermark-to-pdf.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/convertAPI/latest/actions/add-image-watermark-to-pdf).
