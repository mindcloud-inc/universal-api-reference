# Track-POD: Add Route

Creates a new route in Track-POD.

```
POST https://connect.mindcloud.co/v1/universal/trackPOD/latest/actions/add-route
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Track-POD `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/trackPOD/latest/actions/add-route" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/trackPOD/latest/actions/add-route', {
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

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `Code` | string | no | Route code. |
| `Date` | string | no | Route date and time. |
| `Depot` | string | no | Depot name. |
| `DepotId` | string | no | Depot identifier. |
| `DriverLogin` | string | no | Driver login. |
| `DriverName` | string | no | Driver name. |
| `DriverPassword` | string | no | Driver password. |
| `DriverVehicle` | string | no | Driver vehicle. |
| `Id` | string | no | Route identifier. |
| `Orders[0].Address` | string | no | First route order address. |
| `Orders[0].ContactName` | string | no | First route order contact name. |
| `Orders[0].Date` | string | no | First route order date and time. |
| `Orders[0].Note` | string | no | First route order note. |
| `Orders[0].Number` | string | no | First route order number. |
| `Orders[0].Phone` | string | no | First route order phone. |
| `Orders[0].TimeSlotFrom` | string | no | First route order time window start. |
| `Orders[0].TimeSlotTo` | string | no | First route order time window end. |
| `Orders[1].Address` | string | no | Second route order address. |
| `Orders[1].ContactName` | string | no | Second route order contact name. |
| `Orders[1].Date` | string | no | Second route order date and time. |
| `Orders[1].Note` | string | no | Second route order note. |
| `Orders[1].Number` | string | no | Second route order number. |
| `Orders[1].Phone` | string | no | Second route order phone. |
| `Orders[1].TimeSlotFrom` | string | no | Second route order time window start. |
| `Orders[1].TimeSlotTo` | string | no | Second route order time window end. |
| `ReturnToDepot` | boolean | no | Whether the route returns to the depot. Default: `false`. |
| `RouteDate` | string | no | Route date and time. |
| `StartFromDepot` | boolean | no | Whether the route starts from the depot. Default: `true`. |
| `StartTimePlan` | string | no | Planned route start time. |
| `Vehicle.Carrier` | string | no | Route vehicle carrier. |
| `Vehicle.CarrierCode` | string | no | Route vehicle carrier code. |
| `Vehicle.Number` | string | no | Route vehicle number. |
| `Vehicle.Pallets` | number | no | Route vehicle pallet capacity. |
| `Vehicle.Volume` | number | no | Route vehicle volume capacity. |
| `Vehicle.Weight` | number | no | Route vehicle weight capacity. |

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

Through the native Track-POD API, this operation is `POST /Route` (base URL `https://api.track-pod.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-route.md) for the provider-specific parameters and requirements.

