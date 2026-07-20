# Intradesk: List Dashboard Tickets

Retrieves dashboard tickets from Intradesk.

```
GET https://connect.mindcloud.co/v1/universal/intradesk/latest/actions/list-dashboard-tickets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Intradesk `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/intradesk/latest/actions/list-dashboard-tickets?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/intradesk/latest/actions/list-dashboard-tickets?${params}`, {
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
      "aiemotionalassessment": "string",
      "aihistory": "string",
      "customerid": 1,
      "description": "string",
      "id": 1,
      "initiator": 1,
      "name": "Ava Chen",
      "priority": 1,
      "prioritycriticality": 1,
      "priorityinfluence": 1,
      "status": 1,
      "tasknumber": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `aiemotionalassessment` | string |  |
| `aihistory` | string |  |
| `customerid` | number |  |
| `description` | string |  |
| `id` | number |  |
| `initiator` | number |  |
| `name` | string |  |
| `priority` | number |  |
| `prioritycriticality` | number |  |
| `priorityinfluence` | number |  |
| `status` | number |  |
| `tasknumber` | number |  |

## Native endpoint

Through the native Intradesk API, this operation is `GET /tasklist/odata/Dashboard` (base URL `https://apigw.intradesk.ru`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-dashboard-tickets.md) for the provider-specific parameters and requirements.

