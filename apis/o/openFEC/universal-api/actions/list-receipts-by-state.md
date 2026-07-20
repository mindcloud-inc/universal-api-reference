# OpenFEC: List Receipts By State

Retrieves receipt totals in OpenFEC by state.

```
GET https://connect.mindcloud.co/v1/universal/openFEC/latest/actions/list-receipts-by-state
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OpenFEC `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openFEC/latest/actions/list-receipts-by-state?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openFEC/latest/actions/list-receipts-by-state?${params}`, {
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
      "committee_id": "string",
      "committee_name": "Ava Chen",
      "count": 1,
      "cycle": 1,
      "state": "string",
      "state_full": "string",
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `committee_id` | string |  |
| `committee_name` | string |  |
| `count` | number |  |
| `cycle` | number |  |
| `state` | string |  |
| `state_full` | string |  |
| `total` | number |  |

## Native endpoint

Through the native OpenFEC API, this operation is `GET /schedules/schedule_a/by_state/` (base URL `https://api.open.fec.gov/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-receipts-by-state.md) for the provider-specific parameters and requirements.

