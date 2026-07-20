# nandbox Universal API Examples

These examples use the MindCloud API key and nandbox connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Download Media File

Retrieves a media file from nandbox by media ID.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nandbox/latest/actions/download-media-file?connectionId=$CONNECTION_ID&mediaId=123456789.jpg" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "mediaId": "123456789.jpg"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nandbox/latest/actions/download-media-file?${params}`, {
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
      "response": {}
    }
  ],
  "meta": {}
}
```

See the full [Download Media File action reference](actions/download-media-file.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/nandbox/latest/actions/download-media-file).
