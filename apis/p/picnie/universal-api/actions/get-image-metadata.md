# Picnie: Get Image Metadata

Retrieves JPEG image metadata from Picnie.

```
GET https://connect.mindcloud.co/v1/universal/picnie/latest/actions/get-image-metadata
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Picnie `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/picnie/latest/actions/get-image-metadata?connectionId=$CONNECTION_ID&projectId=1&imageUrl=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "1",
  "imageUrl": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/picnie/latest/actions/get-image-metadata?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | number | yes | Project ID for metadata lookup. |
| `imageUrl` | string | yes | JPEG image URL to inspect for metadata. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "error": true,
      "message": "string",
      "metadata": {
        "bits": 1,
        "channels": 1,
        "exif": {
          "computed": {
            "apertureFNumber": "string",
            "byteOrderMotorola": 1,
            "copyright": "string",
            "height": 1,
            "html": "string",
            "isColor": 1,
            "userComment": "string",
            "userCommentEncoding": "string",
            "width": 1
          },
          "exif": {
            "apertureValue": "string",
            "colorSpace": 1,
            "dateTimeDigitized": "string",
            "dateTimeOriginal": "string",
            "digitalZoomRatio": "string",
            "exifImageLength": 1,
            "exifImageWidth": 1,
            "exifVersion": "string",
            "exposureBiasValue": "string",
            "exposureMode": 1,
            "exposureProgram": 1,
            "exposureTime": "string",
            "flash": 1,
            "fNumber": "string",
            "focalLength": "string",
            "focalLengthIn35mmFilm": 1,
            "imageUniqueID": "string",
            "iSOSpeedRatings": 1,
            "maxApertureValue": "string",
            "meteringMode": 1,
            "sceneCaptureType": 1,
            "shutterSpeedValue": "string",
            "undefinedTag:0x9010": "string",
            "undefinedTag:0x9011": "string",
            "whiteBalance": 1
          },
          "file": {
            "fileDateTime": 1,
            "fileSize": 1,
            "fileType": 1,
            "mimeType": "string",
            "sectionsFound": "string"
          },
          "gps": {
            "gPSLatitude": [
              "string"
            ],
            "gPSLatitudeRef": "string",
            "gPSLongitude": [
              "string"
            ],
            "gPSLongitudeRef": "string"
          },
          "ifd0": {
            "artist": "string",
            "copyright": "string",
            "dateTime": "string",
            "dateTimeOriginal": "string",
            "exifIFDPointer": 1,
            "gPSIFDPointer": 1,
            "imageDescription": "string",
            "imageLength": 1,
            "imageWidth": 1,
            "make": "string",
            "model": "string",
            "orientation": 1,
            "resolutionUnit": 1,
            "software": "string",
            "userComment": "string",
            "xResolution": "string",
            "yCbCrPositioning": 1,
            "yResolution": "string"
          }
        },
        "extension": "string",
        "fileSizeBytes": 1,
        "fileSizeKb": 1,
        "height": 1,
        "mimeType": "string",
        "width": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `error` | boolean |  |
| `message` | string |  |
| `metadata.bits` | number |  |
| `metadata.channels` | number |  |
| `metadata.exif.computed.apertureFNumber` | string |  |
| `metadata.exif.computed.byteOrderMotorola` | number |  |
| `metadata.exif.computed.copyright` | string |  |
| `metadata.exif.computed.height` | number |  |
| `metadata.exif.computed.html` | string |  |
| `metadata.exif.computed.isColor` | number |  |
| `metadata.exif.computed.userComment` | string |  |
| `metadata.exif.computed.userCommentEncoding` | string |  |
| `metadata.exif.computed.width` | number |  |
| `metadata.exif.exif.apertureValue` | string |  |
| `metadata.exif.exif.colorSpace` | number |  |
| `metadata.exif.exif.dateTimeDigitized` | string |  |
| `metadata.exif.exif.dateTimeOriginal` | string |  |
| `metadata.exif.exif.digitalZoomRatio` | string |  |
| `metadata.exif.exif.exifImageLength` | number |  |
| `metadata.exif.exif.exifImageWidth` | number |  |
| `metadata.exif.exif.exifVersion` | string |  |
| `metadata.exif.exif.exposureBiasValue` | string |  |
| `metadata.exif.exif.exposureMode` | number |  |
| `metadata.exif.exif.exposureProgram` | number |  |
| `metadata.exif.exif.exposureTime` | string |  |
| `metadata.exif.exif.flash` | number |  |
| `metadata.exif.exif.fNumber` | string |  |
| `metadata.exif.exif.focalLength` | string |  |
| `metadata.exif.exif.focalLengthIn35mmFilm` | number |  |
| `metadata.exif.exif.imageUniqueID` | string |  |
| `metadata.exif.exif.iSOSpeedRatings` | number |  |
| `metadata.exif.exif.maxApertureValue` | string |  |
| `metadata.exif.exif.meteringMode` | number |  |
| `metadata.exif.exif.sceneCaptureType` | number |  |
| `metadata.exif.exif.shutterSpeedValue` | string |  |
| `metadata.exif.exif.undefinedTag:0x9010` | string |  |
| `metadata.exif.exif.undefinedTag:0x9011` | string |  |
| `metadata.exif.exif.whiteBalance` | number |  |
| `metadata.exif.file.fileDateTime` | number |  |
| `metadata.exif.file.fileSize` | number |  |
| `metadata.exif.file.fileType` | number |  |
| `metadata.exif.file.mimeType` | string |  |
| `metadata.exif.file.sectionsFound` | string |  |
| `metadata.exif.gps.gPSLatitude[]` | string |  |
| `metadata.exif.gps.gPSLatitudeRef` | string |  |
| `metadata.exif.gps.gPSLongitude[]` | string |  |
| `metadata.exif.gps.gPSLongitudeRef` | string |  |
| `metadata.exif.ifd0.artist` | string |  |
| `metadata.exif.ifd0.copyright` | string |  |
| `metadata.exif.ifd0.dateTime` | string |  |
| `metadata.exif.ifd0.dateTimeOriginal` | string |  |
| `metadata.exif.ifd0.exifIFDPointer` | number |  |
| `metadata.exif.ifd0.gPSIFDPointer` | number |  |
| `metadata.exif.ifd0.imageDescription` | string |  |
| `metadata.exif.ifd0.imageLength` | number |  |
| `metadata.exif.ifd0.imageWidth` | number |  |
| `metadata.exif.ifd0.make` | string |  |
| `metadata.exif.ifd0.model` | string |  |
| `metadata.exif.ifd0.orientation` | number |  |
| `metadata.exif.ifd0.resolutionUnit` | number |  |
| `metadata.exif.ifd0.software` | string |  |
| `metadata.exif.ifd0.userComment` | string |  |
| `metadata.exif.ifd0.xResolution` | string |  |
| `metadata.exif.ifd0.yCbCrPositioning` | number |  |
| `metadata.exif.ifd0.yResolution` | string |  |
| `metadata.extension` | string |  |
| `metadata.fileSizeBytes` | number |  |
| `metadata.fileSizeKb` | number |  |
| `metadata.height` | number |  |
| `metadata.mimeType` | string |  |
| `metadata.width` | number |  |

## Native endpoint

Through the native Picnie API, this operation is `POST /get-image-metadata` (base URL `https://picnie.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-image-metadata.md) for the provider-specific parameters and requirements.

