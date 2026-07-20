# Encodian - Image: Image - Clean Up Photo

Creates a cleaned-up photo image in Encodian - Image.

```
POST https://connect.mindcloud.co/v1/universal/encodianImage/latest/actions/image-clean-up-photo
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Encodian - Image `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/encodianImage/latest/actions/image-clean-up-photo" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fileName": "Ava Chen",
  "finalOperation": "true",
  "autoRotateConfidenceLevel": "40"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/encodianImage/latest/actions/image-clean-up-photo', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fileName": "Ava Chen",
    "finalOperation": "true",
    "autoRotateConfidenceLevel": "40"
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
| `cleanUpType` | list | no | Clean-up mode to apply. Default performs automatic photo clean-up; None skips clean-up; Specific uses selected advanced clean-up flags. One of: `Default`, `None`, `Specific`. Default: `Default`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `finalOperation` | boolean | yes | Return the processed file content instead of only an operation ID. Default: `true`. |
| `autoRotateConfidenceLevel` | number | yes | Minimum confidence percentage from 0 to 100 used to control whether rotation is applied. Default: `40`. |
| `deskew` | boolean | no | Detects the skew angle and rotates to remove that skew. Default: `true`. |
| `despeckle` | boolean | no | Automatically detects speckles and removes them. Default: `true`. |
| `colorBalance` | boolean | no | Restores and balances image color quality. Default: `true`. |
| `removeBorder` | boolean | no | Locates and removes border pixels from the image. Default: `false`. |
| `contrast` | boolean | no | Adjusts contrast in the image. Default: `false`. |
| `removeRedeye` | boolean | no | Reduces red flash reflection in eyes. Default: `false`. |
| `blur` | boolean | no | Blurs the image by averaging neighboring pixels. Default: `false`. |
| `diffuse` | boolean | no | Diffuses the image by replacing pixels with nearby pixels. Default: `false`. |
| `binarize` | boolean | no | Binarizes the image for dark text on brighter background images. Default: `false`. |
| `autoRotate` | boolean | no | Automatically detects orientation and rotates the image upright. Default: `true`. |

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

Through the native Encodian - Image API, this operation is `POST /api/v1/Image/ImageCleanUpPhoto` (base URL `https://api.apps-encodian.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/image-clean-up-photo.md) for the provider-specific parameters and requirements.

