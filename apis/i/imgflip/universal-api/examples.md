# Imgflip Universal API Examples

These examples use the MindCloud API key and Imgflip connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Popular Memes



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/imgflip/latest/actions/list-popular-memes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/imgflip/latest/actions/list-popular-memes?${params}`, {
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
      "box_count": 1,
      "captions": 1,
      "height": 1,
      "id": "string",
      "name": "Ava Chen",
      "url": "https://example.com",
      "width": 1
    }
  ],
  "meta": {}
}
```

See the full [List Popular Memes action reference](actions/list-popular-memes.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/imgflip/latest/actions/list-popular-memes).

## Caption Image



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/imgflip/latest/actions/caption-image" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "templateId": "string",
  "text0": "string",
  "text1": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/imgflip/latest/actions/caption-image', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "templateId": "string",
    "text0": "string",
    "text1": "string"
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
      "page_url": "https://example.com",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Caption Image action reference](actions/caption-image.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/imgflip/latest/actions/caption-image).
