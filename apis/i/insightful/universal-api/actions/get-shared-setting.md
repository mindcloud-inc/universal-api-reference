# Insightful: Get Shared Setting

Retrieves a shared setting from your Insightful account.

```
GET https://connect.mindcloud.co/v1/universal/insightful/latest/actions/get-shared-setting
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Insightful `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/insightful/latest/actions/get-shared-setting?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/insightful/latest/actions/get-shared-setting?${params}`, {
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
| `id` | string | yes | The shared setting ID. |

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

Through the native Insightful API, this operation is `GET /shared-settings/:id` (base URL `https://app.insightful.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-shared-setting.md) for the provider-specific parameters and requirements.

