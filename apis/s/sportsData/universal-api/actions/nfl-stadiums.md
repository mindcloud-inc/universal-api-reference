# SportsData: NFL Stadiums

Retrieves NFL stadiums from SportsData.

```
GET https://connect.mindcloud.co/v1/universal/sportsData/latest/actions/nfl-stadiums
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SportsData `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sportsData/latest/actions/nfl-stadiums?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sportsData/latest/actions/nfl-stadiums?${params}`, {
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
      "capacity": 1,
      "city": "string",
      "country": "string",
      "geoLat": 1,
      "geoLong": 1,
      "name": "Ava Chen",
      "playingSurface": "string",
      "stadiumID": 1,
      "state": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `capacity` | number | Venue capacity. |
| `city` | string | City. |
| `country` | string | Country. |
| `geoLat` | number | Latitude. |
| `geoLong` | number | Longitude. |
| `name` | string | Stadium name. |
| `playingSurface` | string | Playing surface. |
| `stadiumID` | number | SportsData stadium identifier. |
| `state` | string | State or region. |
| `type` | string | Venue type. |

## Native endpoint

Through the native SportsData API, this operation is `GET /v3/nfl/scores/json/Stadiums` (base URL `https://api.sportsdata.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/nfl-stadiums.md) for the provider-specific parameters and requirements.

