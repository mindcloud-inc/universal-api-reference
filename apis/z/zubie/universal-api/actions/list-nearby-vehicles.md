# Zubie: List Nearby Vehicles

Retrieves nearby vehicles from Zubie.

```
GET https://connect.mindcloud.co/v1/universal/zubie/latest/actions/list-nearby-vehicles
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zubie `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zubie/latest/actions/list-nearby-vehicles?connectionId=$CONNECTION_ID&lat=string&lot=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "lat": "string",
  "lot": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zubie/latest/actions/list-nearby-vehicles?${params}`, {
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
| `lat` | string | yes | Latitude of the point. |
| `lot` | string | yes | Longitude of the point. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "distance_in_miles": 1,
      "key": "string",
      "nickname": "Ava Chen",
      "vehicle_location": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `distance_in_miles` | number |  |
| `key` | string |  |
| `nickname` | string |  |
| `vehicle_location` | object |  |

## Native endpoint

Through the native Zubie API, this operation is `GET /vehicles/nearby` (base URL `https://api.zubiecar.com/api/v2/zinc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-nearby-vehicles.md) for the provider-specific parameters and requirements.

