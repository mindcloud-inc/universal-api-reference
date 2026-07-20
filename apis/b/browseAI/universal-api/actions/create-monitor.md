# Browse AI: Create Monitor

Creates a monitor in Browse AI.

```
POST https://connect.mindcloud.co/v1/universal/browseAI/latest/actions/create-monitor
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Browse AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/browseAI/latest/actions/create-monitor" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "robotId": "c3689adb-50aa-44af-b265-a7e0d4e5846e",
  "name": "Monitor Products",
  "inputParameters": "[object Object]",
  "notifyOnCapturedScreenshotChange": "true",
  "notifyOnCapturedTextChange": "true",
  "capturedScreenshotNotificationThreshold": "15"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/browseAI/latest/actions/create-monitor', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "robotId": "c3689adb-50aa-44af-b265-a7e0d4e5846e",
    "name": "Monitor Products",
    "inputParameters": "[object Object]",
    "notifyOnCapturedScreenshotChange": "true",
    "notifyOnCapturedTextChange": "true",
    "capturedScreenshotNotificationThreshold": "15"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `robotId` | string | yes | Unique robot ID You can find a robot's ID by opening it on the dashboard and copying its ID in the browser address bar. Example: `c3689adb-50aa-44af-b265-a7e0d4e5846e`. |
| `name` | string | yes | Monitor name Example: `Monitor Products`. |
| `inputParameters` | object | yes | An object of input parameters to override default input parameters. Example: `[object Object]`. |
| `schedules[]` | array<object> | no | Array of schedules. Example: `[object Object]`. |
| `schedules[]` | array<object> | no | Array of schedules. Example: `[object Object]`. |
| `schedule` | string | no | recurring schedule. Example: `FREQ=HOURLY;INTERVAL=1;BYWEEKDAY=MO,TU,WE,TH,FR`. |
| `notifyOnCapturedScreenshotChange` | boolean | yes | If set to `true`, an email notification will be sent to you when a change is detected in captured screenshots. Example: `true`. |
| `notifyOnCapturedTextChange` | boolean | yes | If set to `true`, an email notification will be sent to you when a change is detected in captured texts. Example: `true`. |
| `capturedScreenshotNotificationThreshold` | number | yes | The "screenshot changed" email notification will be sent to you if the change is greater than this threshold (in percent). Example: `15`. |

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

Through the native Browse AI API, this operation is `POST /robots/:robotId/monitors` (base URL `https://api.browse.ai/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-monitor.md) for the provider-specific parameters and requirements.

