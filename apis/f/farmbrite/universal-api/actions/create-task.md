# Farmbrite: Create task

Creates a new task in Farmbrite.

```
POST https://connect.mindcloud.co/v1/universal/farmbrite/latest/actions/create-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Farmbrite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/farmbrite/latest/actions/create-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/farmbrite/latest/actions/create-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `title` | string | yes |  |
| `description` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "activitySeriesId": "string",
      "allDay": "string",
      "assignedToId": "string",
      "checklist": [
        "string"
      ],
      "collaboratorIds": [
        "string"
      ],
      "color": "string",
      "complete": true,
      "completedBy": "string",
      "completedOn": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdBy": "string",
      "createdById": "string",
      "description": "string",
      "endTime": "string",
      "frequency": "string",
      "hoursSpent": "string",
      "id": "string",
      "keywords": "string",
      "latitude": "string",
      "longitude": "string",
      "nextOccurrenceId": "string",
      "period": "string",
      "priority": "string",
      "referenceId": "string",
      "referenceType": "string",
      "repeatOnComplete": true,
      "repeatUntil": "string",
      "sourceId": "string",
      "sourceType": "string",
      "startTime": "string",
      "status": "string",
      "teamId": "string",
      "title": "string",
      "todo": true,
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activitySeriesId` | string |  |
| `allDay` | string |  |
| `assignedToId` | string |  |
| `checklist` | array<string> |  |
| `collaboratorIds` | array<string> |  |
| `color` | string |  |
| `complete` | boolean |  |
| `completedBy` | string |  |
| `completedOn` | string |  |
| `createdAt` | date |  |
| `createdBy` | string |  |
| `createdById` | string |  |
| `description` | string |  |
| `endTime` | string |  |
| `frequency` | string |  |
| `hoursSpent` | string |  |
| `id` | string |  |
| `keywords` | string |  |
| `latitude` | string |  |
| `longitude` | string |  |
| `nextOccurrenceId` | string |  |
| `period` | string |  |
| `priority` | string |  |
| `referenceId` | string |  |
| `referenceType` | string |  |
| `repeatOnComplete` | boolean |  |
| `repeatUntil` | string |  |
| `sourceId` | string |  |
| `sourceType` | string |  |
| `startTime` | string |  |
| `status` | string |  |
| `teamId` | string |  |
| `title` | string |  |
| `todo` | boolean |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Farmbrite API, this operation is `POST /tasks` (base URL `https://api.farmbrite.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-task.md) for the provider-specific parameters and requirements.

