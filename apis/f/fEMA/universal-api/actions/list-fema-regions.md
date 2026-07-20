# FEMA: List FEMA Regions

Retrieves FEMA regions.

```
GET https://connect.mindcloud.co/v1/universal/fEMA/latest/actions/list-fema-regions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FEMA `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fEMA/latest/actions/list-fema-regions?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fEMA/latest/actions/list-fema-regions?${params}`, {
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
      "address": "string",
      "city": "string",
      "hash": "string",
      "id": "string",
      "lastRefresh": "2026-05-07T12:00:00.000Z",
      "loc": {},
      "name": "Ava Chen",
      "region": 1,
      "regionGeometry": {},
      "state": "string",
      "states": [
        "string"
      ],
      "zipCode": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string |  |
| `city` | string |  |
| `hash` | string |  |
| `id` | string |  |
| `lastRefresh` | date |  |
| `loc` | object |  |
| `name` | string |  |
| `region` | number |  |
| `regionGeometry` | object |  |
| `state` | string |  |
| `states` | array<string> |  |
| `zipCode` | string |  |

## Native endpoint

Through the native FEMA API, this operation is `GET /v2/FemaRegions` (base URL `https://www.fema.gov/api/open`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-fema-regions.md) for the provider-specific parameters and requirements.

