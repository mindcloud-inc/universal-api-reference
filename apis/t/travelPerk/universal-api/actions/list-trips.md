# TravelPerk: List Trips

Retrieves trips from TravelPerk.

```
GET https://connect.mindcloud.co/v1/universal/travelPerk/latest/actions/list-trips
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TravelPerk `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/travelPerk/latest/actions/list-trips?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/travelPerk/latest/actions/list-trips?${params}`, {
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
| `travelerId` | string | no | Filter trips by the traveler identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "limit": 1,
      "offset": 1,
      "total": 1,
      "trips": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `limit` | number |  |
| `offset` | number |  |
| `total` | number |  |
| `trips` | array<object> |  |

## Native endpoint

Through the native TravelPerk API, this operation is `GET /trips` (base URL `https://api.sandbox-travelperk.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-trips.md) for the provider-specific parameters and requirements.

