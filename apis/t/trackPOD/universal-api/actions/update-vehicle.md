# Track-POD: Update Vehicle

Updates an existing vehicle in Track-POD.

```
PUT https://connect.mindcloud.co/v1/universal/trackPOD/latest/actions/update-vehicle
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Track-POD `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/trackPOD/latest/actions/update-vehicle" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/trackPOD/latest/actions/update-vehicle', {
  method: 'PUT',
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

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `BaseFare` | number | no | Base fare. |
| `Carrier` | string | no | Carrier name. |
| `CarrierCode` | string | no | Carrier code. |
| `CostPerDistance` | number | no | Cost per distance unit. |
| `CostPerHour` | number | no | Cost per hour. |
| `Depot` | string | no | Depot name. |
| `DepotId` | string | no | Depot identifier. |
| `DriverId` | string | no | Assigned driver identifier. |
| `DriverUsername` | string | no | Assigned driver username. |
| `EmissionCo2` | number | no | CO2 emission value. |
| `Id` | string | no | Track-POD unique identifier for the vehicle. |
| `MaxDistance` | number | no | Maximum travel distance. |
| `MaxNodes` | number | no | Maximum route nodes. |
| `MaxWorkTime` | number | no | Maximum work time. |
| `Number` | string | no | Vehicle number. |
| `Pallets` | number | no | Vehicle pallet capacity. |
| `SpeedRatio` | number | no | Speed ratio. |
| `StartTime` | string | no | Vehicle start time. |
| `VehicleType` | string | no | Vehicle type identifier. |
| `Volume` | number | no | Vehicle volume capacity. |
| `Weight` | number | no | Vehicle weight capacity. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Detail": "string",
      "Status": 1,
      "Title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Detail` | string | A human-readable explanation specific to this response. |
| `Status` | number | The HTTP status code for the response |
| `Title` | string | A short, human-readable summary of the response |

## Native endpoint

Through the native Track-POD API, this operation is `PUT /Vehicle` (base URL `https://api.track-pod.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-vehicle.md) for the provider-specific parameters and requirements.

