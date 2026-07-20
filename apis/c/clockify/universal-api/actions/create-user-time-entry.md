# Clockify: Create User Time Entry

Creates a time entry for a user in Clockify.

```
POST https://connect.mindcloud.co/v1/universal/clockify/latest/actions/create-user-time-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clockify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/clockify/latest/actions/create-user-time-entry" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workspaceId": "string",
  "userId": "string",
  "customAttributes[].name": "Ava Chen",
  "customAttributes[].namespace": "Ava Chen",
  "customAttributes[].value": "string",
  "customFields[].customFieldId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clockify/latest/actions/create-user-time-entry', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workspaceId": "string",
    "userId": "string",
    "customAttributes[].name": "Ava Chen",
    "customAttributes[].namespace": "Ava Chen",
    "customAttributes[].value": "string",
    "customFields[].customFieldId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workspaceId` | list<string> | yes |  |
| `userId` | string<string> | yes |  |
| `billable` | boolean | no | Example: `true`. |
| `customAttributes[]` | array<object> | no |  |
| `customFields[]` | array<object> | no |  |
| `description` | string | no | Example: `Example description`. |
| `end` | date | no | Example: `2026-01-01T00:00:00Z`. |
| `projectId` | list<string> | no |  |
| `start` | date | no | Example: `2026-01-01T00:00:00Z`. |
| `tagIds[]` | array<string> | no |  |
| `taskId` | list<string> | no |  |
| `type` | list<string> | no | One of: `BREAK`, `REGULAR`. Example: `STANDARD`. |
| `customAttributes[].name` | string | yes |  |
| `customAttributes[].namespace` | string | yes |  |
| `customAttributes[].value` | string | yes |  |
| `customFields[].customFieldId` | string | yes |  |
| `customFields[].sourceType` | string | no |  |
| `customFields[].value` | object | no |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fromEntry` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "billable": true,
      "customFieldValues": [
        [
          {}
        ]
      ],
      "description": "string",
      "id": "string",
      "isLocked": true,
      "kioskId": "string",
      "projectId": "string",
      "tagIds": [
        [
          "string"
        ]
      ],
      "taskId": "string",
      "timeInterval": {
        "duration": "string",
        "end": "2026-05-07T12:00:00.000Z",
        "start": "2026-05-07T12:00:00.000Z"
      },
      "type": "string",
      "userId": "string",
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `billable` | boolean |  |
| `customFieldValues[]` | array<object> |  |
| `customFieldValues[].customFieldId` | string |  |
| `customFieldValues[].name` | string |  |
| `customFieldValues[].timeEntryId` | string |  |
| `customFieldValues[].type` | string |  |
| `customFieldValues[].value` | object |  |
| `description` | string |  |
| `id` | string |  |
| `isLocked` | boolean |  |
| `kioskId` | string |  |
| `projectId` | string |  |
| `tagIds[]` | array<string> |  |
| `taskId` | string |  |
| `timeInterval` | object |  |
| `timeInterval.duration` | string |  |
| `timeInterval.end` | date |  |
| `timeInterval.start` | date |  |
| `type` | string |  |
| `userId` | string |  |
| `workspaceId` | string |  |

## Native endpoint

Through the native Clockify API, this operation is `POST workspaces/:workspaceId/user/:userId/time-entries` (base URL `https://api.clockify.me/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-user-time-entry.md) for the provider-specific parameters and requirements.

