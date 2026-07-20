# Sumo Logic: List Partitions

Retrieves partitions from your Sumo Logic organization.

```
GET https://connect.mindcloud.co/v1/universal/sumoLogic/latest/actions/list-partitions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sumo Logic `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sumoLogic/latest/actions/list-partitions?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sumoLogic/latest/actions/list-partitions?${params}`, {
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
| `viewTypes[]` | array<string> | no | Partition view types to retrieve. Accepts multiple values as an array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "analyticsTier": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdBy": "string",
      "dataForwardingId": "string",
      "id": "string",
      "indexType": "string",
      "isActive": true,
      "isCompliant": true,
      "isIncludedInDefaultSearch": true,
      "modifiedAt": "2026-05-07T12:00:00.000Z",
      "modifiedBy": "string",
      "name": "Ava Chen",
      "newRetentionPeriod": 1,
      "retentionEffectiveAt": "2026-05-07T12:00:00.000Z",
      "retentionPeriod": 1,
      "routingExpression": "string",
      "totalBytes": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `analyticsTier` | string |  |
| `createdAt` | date |  |
| `createdBy` | string |  |
| `dataForwardingId` | string |  |
| `id` | string |  |
| `indexType` | string |  |
| `isActive` | boolean |  |
| `isCompliant` | boolean |  |
| `isIncludedInDefaultSearch` | boolean |  |
| `modifiedAt` | date |  |
| `modifiedBy` | string |  |
| `name` | string |  |
| `newRetentionPeriod` | number |  |
| `retentionEffectiveAt` | date |  |
| `retentionPeriod` | number |  |
| `routingExpression` | string |  |
| `totalBytes` | number |  |

## Native endpoint

Through the native Sumo Logic API, this operation is `GET /v1/partitions` (base URL `https://api.sumologic.com/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-partitions.md) for the provider-specific parameters and requirements.

