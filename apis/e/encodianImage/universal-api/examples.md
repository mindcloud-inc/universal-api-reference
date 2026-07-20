# Encodian - Image Universal API Examples

These examples use the MindCloud API key and Encodian - Image connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Image - Extract Metadata

Retrieves image metadata from Encodian - Image.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/encodianImage/latest/actions/image-extract-metadata?connectionId=$CONNECTION_ID&fileContent=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fileContent": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/encodianImage/latest/actions/image-extract-metadata?${params}`, {
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
      "bitsPerPixel": 1,
      "Errors": [
        "string"
      ],
      "exifDataJson": "string",
      "fileSize": "string",
      "hasExifData": true,
      "hasXmpData": true,
      "height": 1,
      "horizontalResolution": 1,
      "HttpStatusCode": 1,
      "HttpStatusMessage": "string",
      "imageFormat": "string",
      "OperationId": "string",
      "OperationStatus": "string",
      "orientation": "string",
      "verticalResolution": 1,
      "width": 1
    }
  ],
  "meta": {}
}
```

See the full [Image - Extract Metadata action reference](actions/image-extract-metadata.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/encodianImage/latest/actions/image-extract-metadata).

## Image - Add Image Watermark

Creates an image with an image watermark in Encodian - Image.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/encodianImage/latest/actions/image-add-image-watermark" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "filename": "Ava Chen",
  "fileContent": "string",
  "watermarkFilename": "Ava Chen",
  "watermarkFileContent": "string",
  "watermarkPosition": "CentreHorizontal"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/encodianImage/latest/actions/image-add-image-watermark', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "filename": "Ava Chen",
    "fileContent": "string",
    "watermarkFilename": "Ava Chen",
    "watermarkFileContent": "string",
    "watermarkPosition": "CentreHorizontal"
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
      "Errors": [
        "string"
      ],
      "FileContent": "string",
      "Filename": "Ava Chen",
      "HttpStatusCode": 1,
      "HttpStatusMessage": "string",
      "OperationId": "string",
      "OperationStatus": "string"
    }
  ],
  "meta": {}
}
```

See the full [Image - Add Image Watermark action reference](actions/image-add-image-watermark.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/encodianImage/latest/actions/image-add-image-watermark).
