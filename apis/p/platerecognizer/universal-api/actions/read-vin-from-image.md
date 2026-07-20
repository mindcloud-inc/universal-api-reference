# Platerecognizer: Read VIN From Image

Reads a VIN from an image with Plate Recognizer.

```
GET https://connect.mindcloud.co/v1/universal/platerecognizer/latest/actions/read-vin-from-image
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Platerecognizer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/platerecognizer/latest/actions/read-vin-from-image?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/platerecognizer/latest/actions/read-vin-from-image?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `cameraId` | string | no | Unique camera identifier. |
| `timestamp` | date | no | UTC ISO 8601 timestamp for the capture. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cameraId": "string",
      "filename": "Ava Chen",
      "processingTime": 1,
      "results": [
        {
          "identifier": {
            "props": {
              "code": [
                {
                  "value": "string"
                }
              ],
              "confidence": 1,
              "orientation": [
                {
                  "value": "string"
                }
              ]
            },
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
| `processingTime` | number |  |
| `results[].identifier.props.code[].value` | string |  |
| `results[].identifier.props.confidence` | number |  |
| `results[].identifier.props.orientation[].value` | string |  |
| `results[].identifier.type` | string |  |
| `timestamp` | date |  |
| `version` | number |  |

## Native endpoint

Through the native Platerecognizer API, this operation is `POST /vin/reader/` (base URL `https://api.platerecognizer.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/read-vin-from-image.md) for the provider-specific parameters and requirements.

