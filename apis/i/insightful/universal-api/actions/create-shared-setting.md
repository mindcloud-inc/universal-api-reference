# Insightful: Create Shared Setting

Creates a new shared setting in Insightful.

```
POST https://connect.mindcloud.co/v1/universal/insightful/latest/actions/create-shared-setting
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Insightful `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/insightful/latest/actions/create-shared-setting" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "settings": {},
  "type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/insightful/latest/actions/create-shared-setting', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "settings": {},
    "type": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `description` | string | no | A description for the shared settings. |
| `name` | string | yes | The shared settings name. |
| `settings` | object | yes | The shared settings payload object. |
| `type` | string | yes | The settings type. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "default": true,
      "description": "string",
      "id": "string",
      "modelName": "Ava Chen",
      "name": "Ava Chen",
      "organizationId": "string",
      "settings": {
        "breaks": 1,
        "breakTime": {
          "type": "string"
        },
        "clocker": true,
        "days": {
          "friday": true,
          "monday": true,
          "saturday": true,
          "sunday": true,
          "thursday": true,
          "tuesday": true,
          "wednesday": true
        },
        "icon": true,
        "idle": 1,
        "idleScreenshots": true,
        "privileges": {
          "apps": true,
          "manualTime": true,
          "manualTimeCreate": true,
          "offline": true,
          "pm": true,
          "productivity": true,
          "screenshots": true,
          "shiftScheduling": true
        },
        "screenshots": 1,
        "security": {
          "timeSync": true
        },
        "timer": true,
        "trackOutsideScheduledShift": true,
        "type": "string"
      },
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `default` | boolean |  |
| `description` | string |  |
| `id` | string |  |
| `modelName` | string |  |
| `name` | string |  |
| `organizationId` | string |  |
| `settings.breaks` | number |  |
| `settings.breakTime.type` | string |  |
| `settings.clocker` | boolean |  |
| `settings.days.friday` | boolean |  |
| `settings.days.monday` | boolean |  |
| `settings.days.saturday` | boolean |  |
| `settings.days.sunday` | boolean |  |
| `settings.days.thursday` | boolean |  |
| `settings.days.tuesday` | boolean |  |
| `settings.days.wednesday` | boolean |  |
| `settings.icon` | boolean |  |
| `settings.idle` | number |  |
| `settings.idleScreenshots` | boolean |  |
| `settings.privileges.apps` | boolean |  |
| `settings.privileges.manualTime` | boolean |  |
| `settings.privileges.manualTimeCreate` | boolean |  |
| `settings.privileges.offline` | boolean |  |
| `settings.privileges.pm` | boolean |  |
| `settings.privileges.productivity` | boolean |  |
| `settings.privileges.screenshots` | boolean |  |
| `settings.privileges.shiftScheduling` | boolean |  |
| `settings.screenshots` | number |  |
| `settings.security.timeSync` | boolean |  |
| `settings.timer` | boolean |  |
| `settings.trackOutsideScheduledShift` | boolean |  |
| `settings.type` | string |  |
| `type` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Insightful API, this operation is `POST /shared-settings` (base URL `https://app.insightful.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-shared-setting.md) for the provider-specific parameters and requirements.

