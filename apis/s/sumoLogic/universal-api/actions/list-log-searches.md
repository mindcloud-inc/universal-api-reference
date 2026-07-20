# Sumo Logic: List Log Searches

Retrieves saved log searches from Sumo Logic.

```
GET https://connect.mindcloud.co/v1/universal/sumoLogic/latest/actions/list-log-searches
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sumo Logic `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sumoLogic/latest/actions/list-log-searches?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sumoLogic/latest/actions/list-log-searches?${params}`, {
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
      "description": "string",
      "id": "string",
      "intervalTimeType": "string",
      "modifiedAt": "2026-05-07T12:00:00.000Z",
      "modifiedBy": "string",
      "name": "Ava Chen",
      "parentId": "string",
      "parsingMode": "string",
      "properties": "string",
      "queryParameters": [
        {
          "dataType": "string",
          "description": "string",
          "name": "Ava Chen",
          "value": "string"
        }
      ],
      "queryString": "string",
      "runByReceiptTime": true,
      "schedule": {
        "cronExpression": "string",
        "displayableTimeRange": "string",
        "muteErrorEmails": true,
        "notification": {
          "taskType": "string"
        },
        "parameters": [
          {
            "name": "Ava Chen",
            "value": "string"
          }
        ],
        "parseableTimeRange": {
          "type": "string"
        },
        "scheduleType": "string",
        "threshold": {
          "count": 1,
          "operator": "string",
          "thresholdType": "string"
        },
        "timeZone": "string"
      },
      "timeRange": {
        "type": "string"
      }
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
| `description` | string |  |
| `id` | string |  |
| `intervalTimeType` | string |  |
| `modifiedAt` | date |  |
| `modifiedBy` | string |  |
| `name` | string |  |
| `parentId` | string |  |
| `parsingMode` | string |  |
| `properties` | string |  |
| `queryParameters[].dataType` | string |  |
| `queryParameters[].description` | string |  |
| `queryParameters[].name` | string |  |
| `queryParameters[].value` | string |  |
| `queryString` | string |  |
| `runByReceiptTime` | boolean |  |
| `schedule.cronExpression` | string |  |
| `schedule.displayableTimeRange` | string |  |
| `schedule.muteErrorEmails` | boolean |  |
| `schedule.notification.taskType` | string |  |
| `schedule.parameters[].name` | string |  |
| `schedule.parameters[].value` | string |  |
| `schedule.parseableTimeRange.type` | string |  |
| `schedule.scheduleType` | string |  |
| `schedule.threshold.count` | number |  |
| `schedule.threshold.operator` | string |  |
| `schedule.threshold.thresholdType` | string |  |
| `schedule.timeZone` | string |  |
| `timeRange.type` | string |  |

## Native endpoint

Through the native Sumo Logic API, this operation is `GET /v1/logSearches` (base URL `https://api.sumologic.com/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-log-searches.md) for the provider-specific parameters and requirements.

