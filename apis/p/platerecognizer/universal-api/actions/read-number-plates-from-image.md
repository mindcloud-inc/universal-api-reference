# Platerecognizer: Read Number Plates From Image

Reads vehicle number plates from an image with Plate Recognizer.

```
GET https://connect.mindcloud.co/v1/universal/platerecognizer/latest/actions/read-number-plates-from-image
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Platerecognizer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/platerecognizer/latest/actions/read-number-plates-from-image?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/platerecognizer/latest/actions/read-number-plates-from-image?${params}`, {
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
| `uploadUrl` | string | no | Public URL of the image to process. |
| `upload` | file | no | Image file bytes or a base64-encoded image. |
| `regions` | string | no | Comma-separated country or state codes to bias plate matching. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `cameraId` | string | no | Unique camera identifier. |
| `timestamp` | date | no | UTC ISO 8601 timestamp for the capture. |
| `mmc` | boolean | no | Set true to include make, model, orientation, color, and year when your plan includes this add-on. |
| `direction` | boolean | no | Set true to predict direction of travel. Requires mmc=true. |
| `config` | object | no | Additional engine configuration as JSON. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cameraId": "string",
      "filename": "Ava Chen",
      "imageHeight": 1,
      "imageWidth": 1,
      "processingTime": 1,
      "results": [
        {
          "box": {
            "xmax": 1,
            "xmin": 1,
            "ymax": 1,
            "ymin": 1
          },
          "candidates": [
            {
              "plate": "string",
              "score": 1
            }
          ],
          "dscore": 1,
          "plate": "string",
          "region": {
            "code": "string",
            "score": 1
          },
          "score": 1,
          "vehicle": {
            "box": {
              "xmax": 1,
              "xmin": 1,
              "ymax": 1,
              "ymin": 1
            },
            "score": 1,
            "type": "string"
          }
        }
      ],
      "timestamp": "2026-05-07T12:00:00.000Z",
      "version": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cameraId` | string |  |
| `filename` | string |  |
| `imageHeight` | number |  |
| `imageWidth` | number |  |
| `processingTime` | number |  |
| `results[].box.xmax` | number |  |
| `results[].box.xmin` | number |  |
| `results[].box.ymax` | number |  |
| `results[].box.ymin` | number |  |
| `results[].candidates[].plate` | string |  |
| `results[].candidates[].score` | number |  |
| `results[].dscore` | number |  |
| `results[].plate` | string |  |
| `results[].region.code` | string |  |
| `results[].region.score` | number |  |
| `results[].score` | number |  |
| `results[].vehicle.box.xmax` | number |  |
| `results[].vehicle.box.xmin` | number |  |
| `results[].vehicle.box.ymax` | number |  |
| `results[].vehicle.box.ymin` | number |  |
| `results[].vehicle.score` | number |  |
| `results[].vehicle.type` | string |  |
| `timestamp` | date |  |
| `version` | number |  |

## Native endpoint

Through the native Platerecognizer API, this operation is `POST /plate-reader/` (base URL `https://api.platerecognizer.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/read-number-plates-from-image.md) for the provider-specific parameters and requirements.

