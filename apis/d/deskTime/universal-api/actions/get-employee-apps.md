# DeskTime: Get Employee Apps

Retrieves an employee's tracked apps from DeskTime for a date.

```
GET https://connect.mindcloud.co/v1/universal/deskTime/latest/actions/get-employee-apps
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DeskTime `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deskTime/latest/actions/get-employee-apps?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/deskTime/latest/actions/get-employee-apps?${params}`, {
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
| `id` | string | no | Employee ID. |
| `date` | string | no | Date in YYYY-MM-DD format. Example: `2026-03-24`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "activeProject": [
        {}
      ],
      "afterWorkTime": 1,
      "apps": {},
      "arrived": true,
      "atWorkTime": 1,
      "beforeWorkTime": 1,
      "desktimeTime": 1,
      "efficiency": 1,
      "email": "ava@example.com",
      "group": "string",
      "groupId": 1,
      "id": 1,
      "isOnline": true,
      "late": true,
      "left": true,
      "name": "Ava Chen",
      "notes": [
        {}
      ],
      "offlineTime": 1,
      "onlineTime": 1,
      "productiveTime": 1,
      "productivity": 1,
      "profileUrl": "https://example.com",
      "timezone": "string",
      "work_ends": "string",
      "work_starts": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activeProject` | array<object> |  |
| `afterWorkTime` | number |  |
| `apps` | object |  |
| `arrived` | boolean |  |
| `atWorkTime` | number |  |
| `beforeWorkTime` | number |  |
| `desktimeTime` | number |  |
| `efficiency` | number |  |
| `email` | string |  |
| `group` | string |  |
| `groupId` | number |  |
| `id` | number |  |
| `isOnline` | boolean |  |
| `late` | boolean |  |
| `left` | boolean |  |
| `name` | string |  |
| `notes` | array<object> |  |
| `offlineTime` | number |  |
| `onlineTime` | number |  |
| `productiveTime` | number |  |
| `productivity` | number |  |
| `profileUrl` | string |  |
| `timezone` | string |  |
| `work_ends` | string |  |
| `work_starts` | string |  |

## Native endpoint

Through the native DeskTime API, this operation is `GET /employee/apps` (base URL `https://desktime.com/api/v2/json`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-employee-apps.md) for the provider-specific parameters and requirements.

