# PDF4me Image Universal API Examples

These examples use the MindCloud API key and PDF4me Image connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Image Metadata

Retrieves metadata for an image in PDF4me Image.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pDF4meImage/latest/actions/get-image-metadata?connectionId=$CONNECTION_ID&docContent=string&docName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "docContent": "string",
  "docName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pDF4meImage/latest/actions/get-image-metadata?${params}`, {
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
      "bitsperPixel": 1,
      "fileSize": 1,
      "hasExifData": true,
      "hasXmpData": true,
      "height": 1,
      "horizontalResolution": 1,
      "imageFormat": "string",
      "verticalResolution": 1,
      "width": 1
    }
  ],
  "meta": {}
}
```

See the full [Get Image Metadata action reference](actions/get-image-metadata.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pDF4meImage/latest/actions/get-image-metadata).
