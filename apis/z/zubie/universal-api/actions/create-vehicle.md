# Zubie: Create Vehicle

Creates a vehicle in Zubie.

```
POST https://connect.mindcloud.co/v1/universal/zubie/latest/actions/create-vehicle
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zubie `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zubie/latest/actions/create-vehicle" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zubie/latest/actions/create-vehicle', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
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

Through the native Zubie API, this operation is `POST /vehicles` (base URL `https://api.zubiecar.com/api/v2/zinc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-vehicle.md) for the provider-specific parameters and requirements.

