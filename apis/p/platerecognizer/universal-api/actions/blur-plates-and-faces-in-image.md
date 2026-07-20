# Platerecognizer: Blur Plates And Faces In Image

Blurs plates and faces in an image with Plate Recognizer.

```
GET https://connect.mindcloud.co/v1/universal/platerecognizer/latest/actions/blur-plates-and-faces-in-image
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Platerecognizer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/platerecognizer/latest/actions/blur-plates-and-faces-in-image?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/platerecognizer/latest/actions/blur-plates-and-faces-in-image?${params}`, {
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
| `uploadUrl` | string | no | Public URL of the image to blur. |
| `upload` | file | no | Image file to blur. |
| `plates` | number | no | Blur intensity for detected license plates. |
| `faces` | number | no | Blur intensity for detected faces. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `regions` | string | no | Comma-separated regions forwarded to Snapshot. |
| `cameraId` | string | no | Override configuration camera ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "blur": {
        "base64": "string",
        "contentType": "string",
        "filename": "Ava Chen"
      },
      "faces": [
        {
          "box": {
            "xmax": 1,
            "xmin": 1,
            "ymax": 1,
            "ymin": 1
          },
          "score": 1
        }
      ],
      "plates": [
        {
          "polygon[]": [
            1
          ],
          "result": {}
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `blur.base64` | string |  |
| `blur.contentType` | string |  |
| `blur.filename` | string |  |
| `faces[].box.xmax` | number |  |
| `faces[].box.xmin` | number |  |
| `faces[].box.ymax` | number |  |
| `faces[].box.ymin` | number |  |
| `faces[].score` | number |  |
| `plates[].polygon[][]` | number |  |
| `plates[].result` | object |  |

## Native endpoint

Through the native Platerecognizer API, this operation is `POST https://blur.platerecognizer.com/v1/blur` (base URL `https://api.platerecognizer.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/blur-plates-and-faces-in-image.md) for the provider-specific parameters and requirements.

