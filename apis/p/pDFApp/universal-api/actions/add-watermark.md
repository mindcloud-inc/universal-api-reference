# PDF-app: Add Watermark

Updates a PDF with a watermark in PDF-app.

```
PUT https://connect.mindcloud.co/v1/universal/pDFApp/latest/actions/add-watermark
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PDF-app `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/pDFApp/latest/actions/add-watermark" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fileUrl": "https://www.w3.org/WAI/ER/tests/xhtml/testfiles/resources/pdf/dummy.pdf"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pDFApp/latest/actions/add-watermark', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fileUrl": "https://www.w3.org/WAI/ER/tests/xhtml/testfiles/resources/pdf/dummy.pdf"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fileUrl` | string | yes | File URL to watermark. Example: `https://www.w3.org/WAI/ER/tests/xhtml/testfiles/resources/pdf/dummy.pdf`. |
| `fileName` | string | no | Desired output file name. Example: `watermarked-dummy`. |
| `fontType` | string | no | PDF text watermark font type. Example: `Helvetica`. |
| `customFont` | string | no | Custom font download URL for text watermarks. Example: `https://raw.githubusercontent.com/notofonts/noto-cjk/main/Sans/OTF/Korean/NotoSansCJKkr-Regular.otf`. |
| `watermarkText` | string | no | Text to use as the watermark. Example: `MindCloud`. |
| `textColor` | string | no | Hex color for the text watermark. Example: `#000000`. |
| `textOpacity` | number | no | Opacity for the text watermark. Example: `0.5`. |
| `fontSize` | number | no | Font size for the text watermark. Example: `18`. |
| `placement` | string | no | Placement preset for the watermark. Example: `center`. |
| `textAngle` | number | no | Rotation angle for the text watermark. Example: `45`. |
| `horizontal_margine` | number | no | Horizontal offset for the watermark. Example: `0`. |
| `vertical_margine` | number | no | Vertical offset for the watermark. Example: `0`. |
| `pageRange` | string | no | Page range to apply the watermark to. Example: `2-5`. |
| `watermarkImageUrl` | string | no | Optional image URL to use as the watermark. Example: `https://example.com/watermark.png`. |
| `imageAngle` | number | no | Rotation angle for the image watermark. Example: `45`. |
| `imageScale` | number | no | Scale factor for the image watermark. Example: `1`. |
| `imageOpacity` | number | no | Opacity for the image watermark. Example: `0.5`. |
| `fixedWidth` | number | no | Fixed width for the image watermark. Example: `200`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "creditsConsumed": 1,
      "creditsRemaining": 1,
      "job_id": "string",
      "message": "string",
      "presignedUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `creditsConsumed` | number | Credits consumed by the operation |
| `creditsRemaining` | number | Remaining account credits after the run |
| `job_id` | string | Processing job identifier |
| `message` | string | Provider success message |
| `presignedUrl` | string | Temporary download URL for the watermarked file |

## Native endpoint

Through the native PDF-app API, this operation is `POST /waterMark` (base URL `https://api.pdf-app.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-watermark.md) for the provider-specific parameters and requirements.

