# Samsara: Get Vehicle Locations



```
GET https://connect.mindcloud.co/v1/universal/samsara/latest/actions/get-vehicle-locations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Samsara `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/samsara/latest/actions/get-vehicle-locations?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/samsara/latest/actions/get-vehicle-locations?${params}`, {
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
      "id": "string",
      "location": {
        "heading": 1,
        "latitude": 1,
        "longitude": 1,
        "reverseGeo": {
          "formattedLocation": "string"
        },
        "speed": 1,
        "time": "string"
      },
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `location.heading` | number |  |
| `location.latitude` | number |  |
| `location.longitude` | number |  |
| `location.reverseGeo.formattedLocation` | string |  |
| `location.speed` | number |  |
| `location.time` | string |  |
| `name` | string |  |

## Native endpoint

Through the native Samsara API, this operation is `GET fleet/vehicles/locations` (base URL `https://api.samsara.com/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-vehicle-locations.md) for the provider-specific parameters and requirements.

