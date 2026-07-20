# Browse AI Universal API Examples

These examples use the MindCloud API key and Browse AI connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Robots

Retrieves robots from Browse AI.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/browseAI/latest/actions/list-robots?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/browseAI/latest/actions/list-robots?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "createdAt": 1,
      "id": "string",
      "inputParameters": [
        {}
      ],
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [List Robots action reference](actions/list-robots.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/browseAI/latest/actions/list-robots).

## Create Monitor

Creates a monitor in Browse AI.

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

Example response:

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

See the full [Create Monitor action reference](actions/create-monitor.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/browseAI/latest/actions/create-monitor).
