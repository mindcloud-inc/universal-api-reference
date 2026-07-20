# Zubie: List Vehicles

Retrieves vehicles from Zubie.

```
GET https://connect.mindcloud.co/v1/universal/zubie/latest/actions/list-vehicles
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zubie `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zubie/latest/actions/list-vehicles?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zubie/latest/actions/list-vehicles?${params}`, {
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
      "key": "string",
      "nickname": "Ava Chen",
      "odometer": 1,
      "plate_number": "string",
      "vehicle_location": {},
      "vin": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `key` | string |  |
| `nickname` | string |  |
| `odometer` | number |  |
| `plate_number` | string |  |
| `vehicle_location` | object |  |
| `vin` | string |  |

## Native endpoint

Through the native Zubie API, this operation is `GET /vehicles` (base URL `https://api.zubiecar.com/api/v2/zinc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-vehicles.md) for the provider-specific parameters and requirements.

