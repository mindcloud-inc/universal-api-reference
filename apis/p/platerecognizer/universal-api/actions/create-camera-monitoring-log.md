# Platerecognizer: Create Camera Monitoring Log

Creates a camera monitoring log in Plate Recognizer VisionAlert.

```
POST https://connect.mindcloud.co/v1/universal/platerecognizer/latest/actions/create-camera-monitoring-log
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Platerecognizer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/platerecognizer/latest/actions/create-camera-monitoring-log" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "cameraId": "string",
  "upload": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/platerecognizer/latest/actions/create-camera-monitoring-log', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "cameraId": "string",
    "upload": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `cameraId` | string | yes | Unique camera identifier for the camera submitting the image. |
| `upload` | file | yes | Image file to analyze for camera issues. |
| `tag` | string | no | Tag to associate with the camera. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |

## Native endpoint

Through the native Platerecognizer API, this operation is `POST /vision-alert/create-log/` (base URL `https://api.platerecognizer.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-camera-monitoring-log.md) for the provider-specific parameters and requirements.

