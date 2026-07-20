# Fleetio: Update Vehicle

Updates an existing vehicle in Fleetio.

```
PUT https://connect.mindcloud.co/v1/universal/fleetio/latest/actions/update-vehicle
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fleetio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/fleetio/latest/actions/update-vehicle" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fleetio/latest/actions/update-vehicle', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The Fleetio ID of the relevant Vehicle. You may also look up Vehicles by their VIN, license plate, or other external ID. See the guide on [External Vehicle Ids](/docs/guides/vehicles/external-vehicle-ids) for information on how to set this up. |
| `color` | string | no | The color of this Vehicle. |
| `fuelTypeId` | number | no | The ID of the `Fuel Type` associated with this Vehicle. |
| `fuelVolumeUnits` | string | no |  |
| `groupId` | number | no |  |
| `groupHierarchy` | string | no | A pipe delimited group hierarchy. Ex: "Level 1\|Level 2\|Level 3". Where Level 1 is the parent of Level 2, and 2 is the parent of 3. Any missing nodes in the hierarchy will be created. |
| `labelIds` | array<number> | no | The `label_id`(s) of any Labels to assign to this Vehicle. If you wish to keep any existing Labels, those IDs must be included in this array as well. |
| `licensePlate` | string | no | The license plate number of this Vehicle. |
| `make` | string | no | The name of this Vehicle's manufacturer. |
| `meterUnit` | string | no | The measurement unit used for the Vehicle's primary, or secondary (if applicable), meter. |
| `model` | string | no | The name of the model of this Vehicle. |
| `name` | string | no | A name to assign to this Vehicle. Must be unique. |
| `ownership` | string | no |  |
| `registrationExpirationMonth` | number | no | The month in which this Vehicle's registration expires. |
| `registrationState` | string | no | The state, province, or territory in which this Vehicle is registered. |
| `secondaryMeter` | boolean | no | Indicates whether or not this Vehicle has a secondary meter. |
| `secondaryMeterUnit` | string | no | The measurement unit used for the Vehicle's primary, or secondary (if applicable), meter. |
| `systemOfMeasurement` | string | no |  |
| `trim` | string | no | The trim level of this Vehicle. |
| `vehicleStatusId` | number | no |  |
| `vehicleTypeId` | number | no |  |
| `vin` | string | no | The Vehicle Identification Number of this Vehicle. Must be unique. |
| `year` | number | no | This Vehicle's model year. |
| `linkedVehicleIds` | array<number> | no | The `vehicle_id`(s) of any Vehicles to link to this Vehicle. |
| `purchaseDetailAttributes` | object | no |  |
| `externalIds` | object | no | Any [External IDs](/docs/guides/vehicles/external-vehicle-ids) associated with this Vehicle. |
| `vehicleStatusName` | string | no | The name of the `Vehicle Status` associated with this Vehicle. |
| `vehicleTypeName` | string | no | The name of the `Vehicle Type` associated with this Vehicle. |
| `inServiceDate` | date | no | The date on which this Vehicle was put into service. We recommend using [ISO-8601](/docs/overview/date-formatting) formatted dates to avoid ambiguity. |
| `inServiceMeter` | number | no | The meter value at which this Vehicle was put into service. |
| `estimatedServiceMonths` | number | no | The estimated number of months this Vehicle will be in service. |
| `estimatedReplacementMileage` | number | no | The estimated number of miles before which this Vehicle will be replaced. |
| `estimatedResalePrice` | number | no | The estimated resale price of this Vehicle. |
| `outOfServiceDate` | date | no | The date on which this Vehicle was or will be retired. We recommend using [ISO-8601](/docs/overview/date-formatting) formatted dates to avoid ambiguity. |
| `outOfServiceMeter` | number | no | The meter value at which this Vehicle was or will be retired. |
| `specsAttributes` | object | no |  |
| `customFields` | object | no | *Full details on working with Custom Fields [here](/docs/overview/custom-fields). |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Fleetio API returns.

## Native endpoint

Through the native Fleetio API, this operation is `PATCH vehicles/:id` (base URL `https://secure.fleetio.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-vehicle.md) for the provider-specific parameters and requirements.

