# Sumo Logic: List Log Data Forwarding Rules

Retrieves S3 data forwarding rules from Sumo Logic.

```
GET https://connect.mindcloud.co/v1/universal/sumoLogic/latest/actions/list-log-data-forwarding-rules
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sumo Logic `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sumoLogic/latest/actions/list-log-data-forwarding-rules?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sumoLogic/latest/actions/list-log-data-forwarding-rules?${params}`, {
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
      "bucket": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdBy": "string",
      "destinationId": "string",
      "enabled": true,
      "fileFormat": "string",
      "format": "string",
      "id": "string",
      "indexId": "string",
      "modifiedAt": "2026-05-07T12:00:00.000Z",
      "modifiedBy": "string",
      "payloadSchema": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bucket` | string |  |
| `createdAt` | date |  |
| `createdBy` | string |  |
| `destinationId` | string |  |
| `enabled` | boolean |  |
| `fileFormat` | string |  |
| `format` | string |  |
| `id` | string |  |
| `indexId` | string |  |
| `modifiedAt` | date |  |
| `modifiedBy` | string |  |
| `payloadSchema` | string |  |

## Native endpoint

Through the native Sumo Logic API, this operation is `GET /v1/logsDataForwarding/rules` (base URL `https://api.sumologic.com/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-log-data-forwarding-rules.md) for the provider-specific parameters and requirements.

