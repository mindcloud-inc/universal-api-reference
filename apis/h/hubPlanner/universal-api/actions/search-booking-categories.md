# Hub Planner: Search Booking Categories

Finds booking categories in Hub Planner by search criteria.

```
GET https://connect.mindcloud.co/v1/universal/hubPlanner/latest/actions/search-booking-categories
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hub Planner `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hubPlanner/latest/actions/search-booking-categories?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hubPlanner/latest/actions/search-booking-categories?${params}`, {
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
      "_id": "string",
      "categoryGroupId": "string",
      "categoryGroupName": "Ava Chen",
      "createdDate": "2026-05-07T12:00:00.000Z",
      "gridColor": "string",
      "name": "Ava Chen",
      "type": "string",
      "updatedDate": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string |  |
| `categoryGroupId` | string |  |
| `categoryGroupName` | string |  |
| `createdDate` | date |  |
| `gridColor` | string |  |
| `name` | string |  |
| `type` | string |  |
| `updatedDate` | date |  |

## Native endpoint

Through the native Hub Planner API, this operation is `POST /categories/search` (base URL `https://api.hubplanner.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-booking-categories.md) for the provider-specific parameters and requirements.

