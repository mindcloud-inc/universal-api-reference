# Track-POD: Get Route By Id

Retrieves a route from Track-POD by ID.

```
GET https://connect.mindcloud.co/v1/universal/trackPOD/latest/actions/get-route-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Track-POD `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/trackPOD/latest/actions/get-route-by-id?connectionId=$CONNECTION_ID&id=route-1001" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "route-1001"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/trackPOD/latest/actions/get-route-by-id?${params}`, {
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
| `id` | string | yes | Track-POD unique identifier for the route. Example: `route-1001`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "CloseDate": "2026-05-07T12:00:00.000Z",
      "Code": "string",
      "CostActual": 1,
      "CostPlan": 1,
      "CreateDateUtc": "2026-05-07T12:00:00.000Z",
      "CustomFields": [
        {}
      ],
      "Date": "2026-05-07T12:00:00.000Z",
      "Depot": "string",
      "DepotId": "string",
      "DistancePlan": 1,
      "DriverLogin": "string",
      "DriverName": "Ava Chen",
      "DriverNumber": 1,
      "DriverVehicle": "string",
      "FinishTimePlan": "2026-05-07T12:00:00.000Z",
      "Id": "string",
      "LocationLat": 1,
      "LocationLon": 1,
      "Orders": [
        {}
      ],
      "Priority": 1,
      "ReturnToDepot": true,
      "StartDate": "2026-05-07T12:00:00.000Z",
      "StartFromDepot": true,
      "StartTimePlan": "2026-05-07T12:00:00.000Z",
      "Status": {},
      "Track": 1,
      "Vehicle": {},
      "Xd": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `CloseDate` | date | Route finish time |
| `Code` | string | Route code/number |
| `CostActual` | number | Actual route cost |
| `CostPlan` | number | Plan route cost |
| `CreateDateUtc` | date | Route creation date (UTC) |
| `CustomFields` | array<object> | List of custom fields |
| `Date` | date | Route date, yyyy-MM-dd |
| `Depot` | string | Depot address |
| `DepotId` | string | Unique identifier in user accounting system |
| `DistancePlan` | number | Planned distance, m |
| `DriverLogin` | string | Driver's login |
| `DriverName` | string | Driver’s First Name and Last Name |
| `DriverNumber` | number | Driver Number |
| `DriverVehicle` | string | Vehicle license plate number |
| `FinishTimePlan` | date | Planned Finish Time |
| `Id` | string | Unique identifier in user accounting system |
| `LocationLat` | number | Current GPS Latitude |
| `LocationLon` | number | Current GPS Longitude |
| `Orders` | array<object> |  |
| `Priority` | number | Route priority |
| `ReturnToDepot` | boolean | Return to depot |
| `StartDate` | date | Route start time |
| `StartFromDepot` | boolean | Start route from depot |
| `StartTimePlan` | date | Planned Start Time |
| `Status` | object |  |
| `Track` | number | Track distance, m |
| `Vehicle` | object |  |
| `Xd` | boolean | Cross-Docking route |

## Native endpoint

Through the native Track-POD API, this operation is `GET /Route/Id/:id` (base URL `https://api.track-pod.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-route-by-id.md) for the provider-specific parameters and requirements.

