# TravelPerk: List Cost Centers

Retrieves cost centers from TravelPerk.

```
GET https://connect.mindcloud.co/v1/universal/travelPerk/latest/actions/list-cost-centers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TravelPerk `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/travelPerk/latest/actions/list-cost-centers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/travelPerk/latest/actions/list-cost-centers?${params}`, {
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
      "cost_centers": [
        {}
      ],
      "limit": 1,
      "offset": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cost_centers` | array<object> |  |
| `limit` | number |  |
| `offset` | number |  |

## Native endpoint

Through the native TravelPerk API, this operation is `GET /cost_centers` (base URL `https://api.sandbox-travelperk.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-cost-centers.md) for the provider-specific parameters and requirements.

