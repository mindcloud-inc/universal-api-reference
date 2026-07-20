# Hub Planner: Search Bookings

Finds bookings in Hub Planner by search criteria.

```
GET https://connect.mindcloud.co/v1/universal/hubPlanner/latest/actions/search-bookings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hub Planner `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hubPlanner/latest/actions/search-bookings?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hubPlanner/latest/actions/search-bookings?${params}`, {
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
      "allDay": true,
      "categoryName": "Ava Chen",
      "createdDate": "2026-05-07T12:00:00.000Z",
      "end": "2026-05-07T12:00:00.000Z",
      "metadata": "string",
      "project": "string",
      "resource": "string",
      "scale": "string",
      "start": "2026-05-07T12:00:00.000Z",
      "state": "string",
      "stateValue": 1,
      "title": "string",
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
| `allDay` | boolean |  |
| `categoryName` | string |  |
| `createdDate` | date |  |
| `end` | date |  |
| `metadata` | string |  |
| `project` | string |  |
| `resource` | string |  |
| `scale` | string |  |
| `start` | date |  |
| `state` | string |  |
| `stateValue` | number |  |
| `title` | string |  |
| `type` | string |  |
| `updatedDate` | date |  |

## Native endpoint

Through the native Hub Planner API, this operation is `POST /booking/search` (base URL `https://api.hubplanner.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-bookings.md) for the provider-specific parameters and requirements.

