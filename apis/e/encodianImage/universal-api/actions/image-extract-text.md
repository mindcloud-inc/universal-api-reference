# Encodian - Image: Image - Extract Text

Retrieves text from an image in Encodian - Image.

```
GET https://connect.mindcloud.co/v1/universal/encodianImage/latest/actions/image-extract-text
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Encodian - Image `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/encodianImage/latest/actions/image-extract-text?connectionId=$CONNECTION_ID&fileName=Ava%20Chen&imageType=PNG&fileContent=string&autoRotateConfidenceLevel=70" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fileName": "Ava Chen",
  "imageType": "PNG",
  "fileContent": "string",
  "autoRotateConfidenceLevel": "70"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/encodianImage/latest/actions/image-extract-text?${params}`, {
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
| `fileName` | string | yes | The filename of the source image file. |
| `imageType` | list | yes | Source image file format for OCR processing. One of: `BMP`, `JPG`, `PNG`, `TIFF`. Default: `PNG`. |
| `fileContent` | string | yes | Base64 content of the source image file. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `autoRotateConfidenceLevel` | number | yes | Minimum confidence percentage from 0 to 100 used to control whether rotation is applied. Default: `70`. |
| `ocrLanguage` | list | no | Language used for OCR processing. Default is English. One of: `Albanian`, `Arabic`, `Azerbaijani`, `Basque`, `Belarusian`, `Bengali`, `Bosnian`, `Bulgarian`, `Burmese`, `Catalan`, `ChineseSimplified`, `ChineseTraditional`, `Croatian`, `Czech`, `Danish`, `Dutch`, `English`, `Estonian`, `Finnish`, `French`, `Georgian`, `German`, `Greek`, `Gujarati`, `Hebrew`, `Hindi`, `Hungarian`, `Icelandic`, `Indonesian`, `Italian`, `Japanese`, `Kannada`, `Kazakh`, `Khmer`, `Korean`, `Kurdish`, `Kyrgyz`, `Laotian`, `Latin`, `Latvian`, `Lithuanian`, `Macedonian`, `Maharashtra`, `Malay`, `Malayalam`, `Maltese`, `Nepali`, `Norwegian`, `Oriya`, `Panjabi`, `Persian`, `Polish`, `Portuguese`, `Pushto`, `Romanian`, `Russian`, `Sanskrit`, `Serbian`, `Singhalese`, `Slovakian`, `Slovenian`, `Spanish`, `Swahili`, `Swedish`, `Syriac`, `Tamil`, `Telugu`, `Thai`, `Turkish`, `Ukrainian`, `Urdu`, `Uzbek`, `Vietnamese`, `Welsh`, `Yiddish`. Default: `English`. |
| `cleanUpType` | list | no | Clean-up mode to apply before OCR processing. Default performs automatic clean-up; None skips clean-up; Specific uses selected advanced clean-up flags. One of: `Default`, `None`, `Specific`. Default: `None`. |
| `autoRotate` | boolean | no | Automatically detects orientation and rotates the image upright before OCR. Default: `false`. |
| `deskew` | boolean | no | Detects the skew angle and rotates to remove that skew before OCR. Default: `false`. |
| `despeckle` | boolean | no | Automatically detects speckles and removes them before OCR. Default: `false`. |
| `adjustBrightnessContrast` | boolean | no | Automatically adjusts brightness and contrast before OCR. Default: `false`. |
| `removeBorder` | boolean | no | Locates and removes border pixels before OCR. Default: `false`. |
| `smoothBackground` | boolean | no | Smooths background colors to reduce noise before OCR. Default: `false`. |
| `smoothObjects` | boolean | no | Smooths object edges in bitonal documents before OCR. Default: `false`. |
| `removeDotShading` | boolean | no | Removes shaded regions from bitonal documents before OCR. Default: `false`. |
| `imageDetergent` | boolean | no | Smooths regions by shifting similar color values toward a central value before OCR. Default: `false`. |
| `applyAverageFilter` | boolean | no | Applies a 3x3 average filter smoothing operation before OCR. Default: `false`. |
| `removeHolePunch` | boolean | no | Detects and removes hole punch marks before OCR. Default: `false`. |
| `binarize` | boolean | no | Binarizes the image before OCR. Default: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Errors": [
        "string"
      ],
      "HttpStatusCode": 1,
      "HttpStatusMessage": "string",
      "OperationId": "string",
      "OperationStatus": "string",
      "Text": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Errors` | array<string> | Error messages, if any. |
| `HttpStatusCode` | number | HTTP status code. |
| `HttpStatusMessage` | string | HTTP status message. |
| `OperationId` | string | Unique Encodian operation ID. |
| `OperationStatus` | string | Encodian operation status. |
| `Text` | string | Text extracted from the image. |

## Native endpoint

Through the native Encodian - Image API, this operation is `POST /api/v1/Image/ImageExtractText` (base URL `https://api.apps-encodian.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/image-extract-text.md) for the provider-specific parameters and requirements.

