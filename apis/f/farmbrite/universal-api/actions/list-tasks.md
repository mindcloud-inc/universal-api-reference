# Farmbrite: List tasks

Retrieves a list of tasks from Farmbrite.

```
GET https://connect.mindcloud.co/v1/universal/farmbrite/latest/actions/list-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Farmbrite `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/farmbrite/latest/actions/list-tasks?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/farmbrite/latest/actions/list-tasks?${params}`, {
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
| `page` | number | no |  |
| `limit` | number | no |  |
| `sortBy` | string | no |  |
| `sortDir` | list | no | One of: `Ascending`, `Descending`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cached": true,
      "currentPage": 1,
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
      "limit": 1,
      "message": "string",
      "success": true,
      "totalPages": 1,
      "totalRecords": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cached` | boolean |  |
| `currentPage` | number |  |
| `data` | array<object> |  |
| `data[].activitySeriesId` | string |  |
| `data[].allDay` | string |  |
| `data[].assignedToId` | string |  |
| `data[].checklist` | array<string> |  |
| `data[].collaboratorIds` | array<string> |  |
| `data[].color` | string |  |
| `data[].complete` | boolean |  |
| `data[].completedBy` | string |  |
| `data[].completedOn` | string |  |
| `data[].createdAt` | date |  |
| `data[].createdBy` | string |  |
| `data[].createdById` | string |  |
| `data[].description` | string |  |
| `data[].endTime` | string |  |
| `data[].frequency` | string |  |
| `data[].hoursSpent` | string |  |
| `data[].id` | string |  |
| `data[].keywords` | string |  |
| `data[].latitude` | string |  |
| `data[].longitude` | string |  |
| `data[].nextOccurrenceId` | string |  |
| `data[].period` | string |  |
| `data[].priority` | string |  |
| `data[].referenceId` | string |  |
| `data[].referenceType` | string |  |
| `data[].repeatOnComplete` | boolean |  |
| `data[].repeatUntil` | string |  |
| `data[].sourceId` | string |  |
| `data[].sourceType` | string |  |
| `data[].startTime` | string |  |
| `data[].status` | string |  |
| `data[].teamId` | string |  |
| `data[].title` | string |  |
| `data[].todo` | boolean |  |
| `data[].updatedAt` | date |  |
| `limit` | number |  |
| `message` | string |  |
| `success` | boolean |  |
| `totalPages` | number |  |
| `totalRecords` | number |  |

## Native endpoint

Through the native Farmbrite API, this operation is `GET /tasks` (base URL `https://api.farmbrite.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-tasks.md) for the provider-specific parameters and requirements.

