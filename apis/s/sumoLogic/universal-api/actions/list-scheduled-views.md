# Sumo Logic: List Scheduled Views

Retrieves scheduled views from your Sumo Logic organization.

```
GET https://connect.mindcloud.co/v1/universal/sumoLogic/latest/actions/list-scheduled-views
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sumo Logic `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sumoLogic/latest/actions/list-scheduled-views?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sumoLogic/latest/actions/list-scheduled-views?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdBy": "string",
      "createdByOptimizeIt": true,
      "dataForwardingId": "string",
      "error": "string",
      "filledRanges": [
        {
          "endTime": "2026-05-07T12:00:00.000Z",
          "startTime": "2026-05-07T12:00:00.000Z"
        }
      ],
      "id": "string",
      "indexId": "string",
      "indexName": "Ava Chen",
      "lastAccessedAt": "2026-05-07T12:00:00.000Z",
      "modifiedAt": "2026-05-07T12:00:00.000Z",
      "modifiedBy": "string",
      "newRetentionPeriod": 1,
      "parsingMode": "string",
      "query": "string",
      "retentionEffectiveAt": "2026-05-07T12:00:00.000Z",
      "retentionPeriod": 1,
      "startTime": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "timeZone": "string",
      "totalBytes": 1,
      "totalMessageCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `createdBy` | string |  |
| `createdByOptimizeIt` | boolean |  |
| `dataForwardingId` | string |  |
| `error` | string |  |
| `filledRanges[].endTime` | date |  |
| `filledRanges[].startTime` | date |  |
| `id` | string |  |
| `indexId` | string |  |
| `indexName` | string |  |
| `lastAccessedAt` | date |  |
| `modifiedAt` | date |  |
| `modifiedBy` | string |  |
| `newRetentionPeriod` | number |  |
| `parsingMode` | string |  |
| `query` | string |  |
| `retentionEffectiveAt` | date |  |
| `retentionPeriod` | number |  |
| `startTime` | date |  |
| `status` | string |  |
| `timeZone` | string |  |
| `totalBytes` | number |  |
| `totalMessageCount` | number |  |

## Native endpoint

Through the native Sumo Logic API, this operation is `GET /v1/scheduledViews` (base URL `https://api.sumologic.com/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-scheduled-views.md) for the provider-specific parameters and requirements.

