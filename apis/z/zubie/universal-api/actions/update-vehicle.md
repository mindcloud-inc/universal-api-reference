# Zubie: Update Vehicle

Updates an existing vehicle in Zubie.

```
PUT https://connect.mindcloud.co/v1/universal/zubie/latest/actions/update-vehicle
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zubie `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zubie/latest/actions/update-vehicle" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "vehicle_key": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zubie/latest/actions/update-vehicle', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "vehicle_key": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `vehicle_key` | string | yes | Unique vehicle key. |

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

Through the native Zubie API, this operation is `POST /vehicle/{vehicle_key}` (base URL `https://api.zubiecar.com/api/v2/zinc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-vehicle.md) for the provider-specific parameters and requirements.

