# Timelink: Update Time Entry

Updates an existing time entry in Timelink.

```
PUT https://connect.mindcloud.co/v1/universal/timelink/latest/actions/update-time-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timelink `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/timelink/latest/actions/update-time-entry" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/timelink/latest/actions/update-time-entry', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes |  |
| `description` | string | no |  |
| `ended_at` | string | no |  |

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

Through the native Timelink API, this operation is `PATCH /timeEntries/:id` (base URL `https://api.timelink.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-time-entry.md) for the provider-specific parameters and requirements.

