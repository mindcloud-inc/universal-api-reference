# Encodian - Image: Image - Clean Up Document

Creates a cleaned-up document image in Encodian - Image.

```
POST https://connect.mindcloud.co/v1/universal/encodianImage/latest/actions/image-clean-up-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Encodian - Image `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/encodianImage/latest/actions/image-clean-up-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fileName": "Ava Chen",
  "finalOperation": "true",
  "autoRotateConfidenceLevel": "60"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/encodianImage/latest/actions/image-clean-up-document', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fileName": "Ava Chen",
    "finalOperation": "true",
    "autoRotateConfidenceLevel": "60"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fileName` | string | yes | The filename of the source image file. The file extension is mandatory. |
| `fileContent` | string | no | Base64 content of the source image file. |
| `cleanUpType` | list | no | Clean-up mode to apply. Default performs automatic document clean-up; None skips clean-up; Specific uses selected advanced clean-up flags. One of: `Default`, `None`, `Specific`. Default: `Default`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `finalOperation` | boolean | yes | Return the processed file content instead of only an operation ID. Default: `true`. |
| `autoRotateConfidenceLevel` | number | yes | Minimum confidence percentage from 0 to 100 used to control whether rotation is applied. Default: `60`. |
| `autoRotate` | boolean | no | Automatically detects orientation and rotates the image upright. Default: `true`. |
| `deskew` | boolean | no | Detects the skew angle and rotates to remove that skew. Default: `true`. |
| `despeckle` | boolean | no | Automatically detects speckles and removes them. Default: `true`. |
| `adjustBrightnessContrast` | boolean | no | Automatically adjusts brightness and contrast based on image analysis. Default: `false`. |
| `removeBorder` | boolean | no | Locates and removes border pixels from the document. Default: `false`. |
| `smoothBackground` | boolean | no | Smooths background colors to reduce noise. Default: `false`. |
| `smoothObjects` | boolean | no | Smooths object edges in bitonal documents. Default: `false`. |
| `removeDotShading` | boolean | no | Removes shaded regions from bitonal documents. Default: `false`. |
| `imageDetergent` | boolean | no | Smooths regions by shifting similar color values toward a central value. Default: `false`. |
| `applyAverageFilter` | boolean | no | Applies a 3x3 average filter smoothing operation. Default: `false`. |
| `removeHolePunch` | boolean | no | Detects and removes hole punch marks from a bitonal document. Default: `false`. |
| `binarize` | boolean | no | Binarizes the image for dark text on brighter background documents. Default: `false`. |

## Response

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

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Errors` | array<string> | Error messages, if any. |
| `FileContent` | string | Base64 content of the processed image. |
| `Filename` | string | The filename of the processed image. |
| `HttpStatusCode` | number | HTTP status code. |
| `HttpStatusMessage` | string | HTTP status message. |
| `OperationId` | string | Unique Encodian operation ID. |
| `OperationStatus` | string | Encodian operation status. |

## Native endpoint

Through the native Encodian - Image API, this operation is `POST /api/v1/Image/ImageCleanUpDocument` (base URL `https://api.apps-encodian.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/image-clean-up-document.md) for the provider-specific parameters and requirements.

