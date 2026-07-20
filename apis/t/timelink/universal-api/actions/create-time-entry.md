# Timelink: Create Time Entry

Creates a time entry in Timelink.

```
POST https://connect.mindcloud.co/v1/universal/timelink/latest/actions/create-time-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timelink `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/timelink/latest/actions/create-time-entry" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "user_id": "string",
  "client_id": "string",
  "started_at": "string",
  "ended_at": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/timelink/latest/actions/create-time-entry', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "user_id": "string",
    "client_id": "string",
    "started_at": "string",
    "ended_at": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `user_id` | string | yes |  |
| `client_id` | string | yes |  |
| `started_at` | string | yes |  |
| `ended_at` | string | yes |  |
| `description` | string | no |  |
| `ext_tool_id` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "billable": true,
      "billedAt": {},
      "clientId": "string",
      "companyId": "string",
      "createdAt": "string",
      "deletedAt": {},
      "description": "string",
      "endedAt": "string",
      "extToolId": "string",
      "id": "string",
      "isInterrupt": true,
      "lastPush": {},
      "paid": true,
      "projectId": {},
      "pushErrors": {},
      "pushState": {},
      "serviceId": {},
      "startedAt": "string",
      "tempId": {},
      "updatedAt": "string",
      "user": {
        "email": "ava@example.com",
        "extToolId": "string",
        "firstName": "Ava",
        "fullName": "Ava Chen",
        "id": "string",
        "lastName": "Chen"
      },
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `billable` | boolean |  |
| `billedAt` | object |  |
| `clientId` | string |  |
| `companyId` | string |  |
| `createdAt` | string |  |
| `deletedAt` | object |  |
| `description` | string |  |
| `endedAt` | string |  |
| `extToolId` | string |  |
| `id` | string |  |
| `isInterrupt` | boolean |  |
| `lastPush` | object |  |
| `paid` | boolean |  |
| `projectId` | object |  |
| `pushErrors` | object |  |
| `pushState` | object |  |
| `serviceId` | object |  |
| `startedAt` | string |  |
| `tempId` | object |  |
| `updatedAt` | string |  |
| `user.email` | string |  |
| `user.extToolId` | string |  |
| `user.firstName` | string |  |
| `user.fullName` | string |  |
| `user.id` | string |  |
| `user.lastName` | string |  |
| `userId` | string |  |

## Native endpoint

Through the native Timelink API, this operation is `POST /timeEntries` (base URL `https://api.timelink.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-time-entry.md) for the provider-specific parameters and requirements.

