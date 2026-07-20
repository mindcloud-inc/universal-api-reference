# Clockify: Create Holiday

Creates a new holiday in Clockify.

```
POST https://connect.mindcloud.co/v1/universal/clockify/latest/actions/create-holiday
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clockify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/clockify/latest/actions/create-holiday" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workspaceId": "string",
  "datePeriod": {},
  "name": "Example Name",
  "automaticTimeEntryCreation.defaultEntities": {},
  "datePeriod.endDate": "string",
  "datePeriod.startDate": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clockify/latest/actions/create-holiday', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workspaceId": "string",
    "datePeriod": {},
    "name": "Example Name",
    "automaticTimeEntryCreation.defaultEntities": {},
    "datePeriod.endDate": "string",
    "datePeriod.startDate": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workspaceId` | list<string> | yes |  |
| `datePeriod` | object | yes |  |
| `name` | string | yes | Example: `Example Name`. |
| `automaticTimeEntryCreation` | object | no |  |
| `color` | string | no |  |
| `everyoneIncludingNew` | boolean | no | Example: `true`. |
| `occursAnnually` | boolean | no | Example: `true`. |
| `userGroups` | object | no |  |
| `users` | object | no |  |
| `automaticTimeEntryCreation.defaultEntities` | object | yes |  |
| `automaticTimeEntryCreation.defaultEntities.projectId` | string | no |  |
| `automaticTimeEntryCreation.defaultEntities.taskId` | string | no |  |
| `automaticTimeEntryCreation.enabled` | boolean | no |  |
| `datePeriod.endDate` | string | yes |  |
| `datePeriod.startDate` | string | yes |  |
| `userGroups.contains` | string | no |  |
| `userGroups.ids[]` | array<string> | no |  |
| `userGroups.status` | string | no |  |
| `users.contains` | string | no |  |
| `users.ids[]` | array<string> | no |  |
| `users.status` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "automaticTimeEntryCreation": true,
      "datePeriod": {
        "endDate": "2026-05-07T12:00:00.000Z",
        "startDate": "2026-05-07T12:00:00.000Z"
      },
      "everyoneIncludingNew": true,
      "id": "string",
      "name": "Ava Chen",
      "occursAnnually": true,
      "projectId": "string",
      "taskId": "string",
      "userGroupIds": [
        [
          "string"
        ]
      ],
      "userIds": [
        [
          "string"
        ]
      ],
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `automaticTimeEntryCreation` | boolean |  |
| `datePeriod` | object |  |
| `datePeriod.endDate` | date |  |
| `datePeriod.startDate` | date |  |
| `everyoneIncludingNew` | boolean |  |
| `id` | string |  |
| `name` | string |  |
| `occursAnnually` | boolean |  |
| `projectId` | string |  |
| `taskId` | string |  |
| `userGroupIds[]` | array<string> |  |
| `userIds[]` | array<string> |  |
| `workspaceId` | string |  |

## Native endpoint

Through the native Clockify API, this operation is `POST workspaces/:workspaceId/holidays` (base URL `https://api.clockify.me/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-holiday.md) for the provider-specific parameters and requirements.

