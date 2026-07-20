# Browse AI: Get Monitor

Retrieves a monitor from Browse AI.

```
GET https://connect.mindcloud.co/v1/universal/browseAI/latest/actions/get-monitor
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Browse AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/browseAI/latest/actions/get-monitor?connectionId=$CONNECTION_ID&robotId=c3689adb-50aa-44af-b265-a7e0d4e5846e&monitorId=e524ab69-4269-4d9d-b3d8-678112a10d29" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "robotId": "c3689adb-50aa-44af-b265-a7e0d4e5846e",
  "monitorId": "e524ab69-4269-4d9d-b3d8-678112a10d29"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/browseAI/latest/actions/get-monitor?${params}`, {
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
| `robotId` | string | yes | Unique robot ID You can find a robot's ID by opening it on the dashboard and copying its ID in the browser address bar. Example: `c3689adb-50aa-44af-b265-a7e0d4e5846e`. |
| `monitorId` | string | yes | Unique monitor ID You can find a monitor's ID by opening it on the dashboard and copying its ID in the browser address bar. Example: `e524ab69-4269-4d9d-b3d8-678112a10d29`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "capturedScreenshotNotificationThreshold": 1,
      "createdAt": 1,
      "id": "string",
      "inputParameters": {},
      "name": "Ava Chen",
      "notifyOnCapturedScreenshotChange": true,
      "notifyOnCapturedTextChange": true,
      "pausedAt": 1,
      "pausedReason": "string",
      "schedule": "string",
      "schedules": [
        {}
      ],
      "status": "string",
      "updatedAt": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `capturedScreenshotNotificationThreshold` | number | The "screenshot changed" email notification will be sent to you if the change is greater than this threshold (in percent). |
| `createdAt` | number | Monitor creation date and time in the form of a Unix timestamp. |
| `id` | string | Unique robot monitor ID |
| `inputParameters` | object | An object of input parameters to override default input parameters. |
| `name` | string | Monitor name |
| `notifyOnCapturedScreenshotChange` | boolean | If set to `true`, an email notification will be sent to you when a change is detected in captured screenshots. |
| `notifyOnCapturedTextChange` | boolean | If set to `true`, an email notification will be sent to you when a change is detected in captured texts. |
| `pausedAt` | number | Monitor pause date and time in the form of a Unix timestamp. |
| `pausedReason` | string | Specifies the reason why the monitor is in a paused state. |
| `schedule` | string | recurring schedule. |
| `schedules` | array<object> | Array of schedules. |
| `status` | string | Represents the current state of the monitor. 'active' indicates that the monitor is currently operational and performing its intended functions, while 'paused' signifies that the monitor's activities are temporarily suspended. The 'paused' state may be due to reasons specified in the 'pausedReason' attribute. |
| `updatedAt` | number | Monitor last update date and time in the form of a Unix timestamp. |

## Native endpoint

Through the native Browse AI API, this operation is `GET /robots/:robotId/monitors/:monitorId` (base URL `https://api.browse.ai/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-monitor.md) for the provider-specific parameters and requirements.

