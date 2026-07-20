# SportsData: NBA Stadiums

Retrieves NBA stadiums from SportsData.

```
GET https://connect.mindcloud.co/v1/universal/sportsData/latest/actions/nba-stadiums
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SportsData `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sportsData/latest/actions/nba-stadiums?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sportsData/latest/actions/nba-stadiums?${params}`, {
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
      "active": true,
      "address": "string",
      "capacity": 1,
      "city": "string",
      "country": "string",
      "geoLat": 1,
      "geoLong": 1,
      "name": "Ava Chen",
      "stadiumID": 1,
      "state": "string",
      "zip": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean | Whether the venue is active. |
| `address` | string | Street address. |
| `capacity` | number | Venue capacity. |
| `city` | string | City. |
| `country` | string | Country. |
| `geoLat` | number | Latitude. |
| `geoLong` | number | Longitude. |
| `name` | string | Stadium name. |
| `stadiumID` | number | SportsData stadium identifier. |
| `state` | string | State or region. |
| `zip` | string | Postal code. |

## Native endpoint

Through the native SportsData API, this operation is `GET /v3/nba/scores/json/Stadiums` (base URL `https://api.sportsdata.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/nba-stadiums.md) for the provider-specific parameters and requirements.

