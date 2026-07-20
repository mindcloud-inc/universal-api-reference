# Clockify: Replace Time Entries

Replaces a user's time entries in Clockify.

```
PUT https://connect.mindcloud.co/v1/universal/clockify/latest/actions/replace-time-entries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clockify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/clockify/latest/actions/replace-time-entries" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workspaceId": "string",
  "userId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clockify/latest/actions/replace-time-entries', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workspaceId": "string",
    "userId": "string"
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `hydrated` | boolean | no | Example: `true`. |

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

Through the native Clockify API, this operation is `PUT workspaces/:workspaceId/user/:userId/time-entries` (base URL `https://api.clockify.me/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/replace-time-entries.md) for the provider-specific parameters and requirements.

