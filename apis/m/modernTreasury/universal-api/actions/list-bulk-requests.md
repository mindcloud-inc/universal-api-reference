# Modern Treasury: List Bulk Requests

Retrieves bulk requests from Modern Treasury.

```
GET https://connect.mindcloud.co/v1/universal/modernTreasury/latest/actions/list-bulk-requests
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Modern Treasury `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/modernTreasury/latest/actions/list-bulk-requests?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/modernTreasury/latest/actions/list-bulk-requests?${params}`, {
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
      "actionType": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "failedResultCount": 1,
      "id": "string",
      "liveMode": true,
      "metadata": {},
      "object": "string",
      "resourceType": "string",
      "status": "string",
      "successResultCount": 1,
      "totalResourceCount": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actionType` | string |  |
| `createdAt` | date |  |
| `failedResultCount` | number |  |
| `id` | string |  |
| `liveMode` | boolean |  |
| `metadata` | object |  |
| `object` | string |  |
| `resourceType` | string |  |
| `status` | string |  |
| `successResultCount` | number |  |
| `totalResourceCount` | number |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Modern Treasury API, this operation is `GET /bulk_requests` (base URL `https://app.moderntreasury.com/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-bulk-requests.md) for the provider-specific parameters and requirements.

