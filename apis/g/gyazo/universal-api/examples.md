# Gyazo Universal API Examples

These examples use the MindCloud API key and Gyazo connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current User

Retrieves the current user from Gyazo.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gyazo/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gyazo/latest/actions/get-current-user?${params}`, {
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
      "user": {}
    }
  ],
  "meta": {}
}
```

See the full [Get Current User action reference](actions/get-current-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/gyazo/latest/actions/get-current-user).

## Upload Image

Uploads a new image to Gyazo.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/gyazo/latest/actions/upload-image" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "imagedata": "Attach binary image content as multipart form data."
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gyazo/latest/actions/upload-image', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "imagedata": "Attach binary image content as multipart form data."
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
      "image_id": "string",
      "permalink_url": "https://example.com",
      "thumb_url": "https://example.com",
      "type": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Upload Image action reference](actions/upload-image.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/gyazo/latest/actions/upload-image).
