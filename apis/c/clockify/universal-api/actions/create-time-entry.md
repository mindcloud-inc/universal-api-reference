# Clockify: Create Time Entry

Creates a new time entry in Clockify.

```
POST https://connect.mindcloud.co/v1/universal/clockify/latest/actions/create-time-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clockify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/clockify/latest/actions/create-time-entry" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workspaceId": "string",
  "start": "2026-05-07T12:00:00.000Z"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clockify/latest/actions/create-time-entry', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workspaceId": "string",
    "start": "2026-05-07T12:00:00.000Z"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workspaceId` | list<string> | yes |  |
| `start` | date | yes |  |
| `end` | date | no |  |
| `description` | string | no |  |
| `projectId` | string | no |  |
| `taskId` | string | no |  |
| `tagIds[]` | array<string> | no |  |
| `billable` | boolean | no |  |
| `type` | string | no |  |
| `customFields[]` | array<object> | no |  |
| `customAttributes[]` | array<object> | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "billable": true,
      "customFieldValues": [
        {}
      ],
      "description": "string",
      "id": "string",
      "isLocked": true,
      "kioskId": "string",
      "projectId": "string",
      "tagIds": [
        "string"
      ],
      "taskId": "string",
      "timeInterval": {},
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
| `customFieldValues` | array<object> |  |
| `description` | string |  |
| `id` | string |  |
| `isLocked` | boolean |  |
| `kioskId` | string |  |
| `projectId` | string |  |
| `tagIds` | array<string> |  |
| `taskId` | string |  |
| `timeInterval` | object |  |
| `type` | string |  |
| `userId` | string |  |
| `workspaceId` | string |  |

## Native endpoint

Through the native Clockify API, this operation is `POST workspaces/:workspaceId/time-entries` (base URL `https://api.clockify.me/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-time-entry.md) for the provider-specific parameters and requirements.

