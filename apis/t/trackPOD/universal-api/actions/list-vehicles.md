# Track-POD: List Vehicles

Retrieves vehicles from Track-POD.

```
GET https://connect.mindcloud.co/v1/universal/trackPOD/latest/actions/list-vehicles
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Track-POD `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/trackPOD/latest/actions/list-vehicles?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/trackPOD/latest/actions/list-vehicles?${params}`, {
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
| `number` | string | no | Optional vehicle number to filter the results. Example: `VAN-42`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "BaseFare": 1,
      "Carrier": "string",
      "CarrierCode": "string",
      "CostPerDistance": 1,
      "CostPerHour": 1,
      "Depot": "string",
      "DepotId": "string",
      "DriverId": "string",
      "DriverUsername": "Ava Chen",
      "EmissionCo2": 1,
      "Id": 1,
      "MaxDistance": 1,
      "MaxNodes": 1,
      "MaxWorkTime": 1,
      "Number": "string",
      "Pallets": 1,
      "SpeedRatio": 1,
      "StartTime": "string",
      "VehicleType": 1,
      "Volume": 1,
      "Weight": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `BaseFare` | number | Base fare |
| `Carrier` | string | Carrier |
| `CarrierCode` | string | Carrier Code |
| `CostPerDistance` | number | Cost per distance (km) |
| `CostPerHour` | number | Cost per hour |
| `Depot` | string | Depot address |
| `DepotId` | string | Unique identifier in user accounting system |
| `DriverId` | string | Driver's Track-POD unique identifier |
| `DriverUsername` | string | Driver's username |
| `EmissionCo2` | number | Vehicle emission g/km or g/mile |
| `Id` | number | Track-POD unique identifier |
| `MaxDistance` | number | Maximum distance, km |
| `MaxNodes` | number | Maximum number of sites/orders |
| `MaxWorkTime` | number | Maximum work time, h |
| `Number` | string | Number |
| `Pallets` | number | Capacity Pallets |
| `SpeedRatio` | number | Speed ratio restriction |
| `StartTime` | string | Start time |
| `VehicleType` | number | Vehicle type: 0 - Truck/Car, 1 - Motorcycle, 2 - Bicycle |
| `Volume` | number | Capacity Volume |
| `Weight` | number | Capacity Weight |

## Native endpoint

Through the native Track-POD API, this operation is `GET /Vehicle` (base URL `https://api.track-pod.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-vehicles.md) for the provider-specific parameters and requirements.

