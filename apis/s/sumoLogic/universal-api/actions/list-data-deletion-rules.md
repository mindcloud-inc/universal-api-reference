# Sumo Logic: List Data Deletion Rules

Retrieves data deletion rules from your Sumo Logic organization.

```
GET https://connect.mindcloud.co/v1/universal/sumoLogic/latest/actions/list-data-deletion-rules
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sumo Logic `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sumoLogic/latest/actions/list-data-deletion-rules?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sumoLogic/latest/actions/list-data-deletion-rules?${params}`, {
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
      "byReceiptTime": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdBy": "string",
      "deletedRanges": [
        {
          "endTime": "2026-05-07T12:00:00.000Z",
          "startTime": "2026-05-07T12:00:00.000Z"
        }
      ],
      "endMillis": 1,
      "error": "string",
      "id": "string",
      "modifiedAt": "2026-05-07T12:00:00.000Z",
      "modifiedBy": "string",
      "parsingMode": "string",
      "query": "string",
      "ruleName": "Ava Chen",
      "ruleReason": "string",
      "startMillis": 1,
      "status": "string",
      "timezone": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `byReceiptTime` | boolean |  |
| `createdAt` | date |  |
| `createdBy` | string |  |
| `deletedRanges[].endTime` | date |  |
| `deletedRanges[].startTime` | date |  |
| `endMillis` | number |  |
| `error` | string |  |
| `id` | string |  |
| `modifiedAt` | date |  |
| `modifiedBy` | string |  |
| `parsingMode` | string |  |
| `query` | string |  |
| `ruleName` | string |  |
| `ruleReason` | string |  |
| `startMillis` | number |  |
| `status` | string |  |
| `timezone` | string |  |

## Native endpoint

Through the native Sumo Logic API, this operation is `GET /v1/dataDeletionRules` (base URL `https://api.sumologic.com/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-data-deletion-rules.md) for the provider-specific parameters and requirements.

