# Fleetio: Create Vehicle

Creates a new vehicle in Fleetio.

```
POST https://connect.mindcloud.co/v1/universal/fleetio/latest/actions/create-vehicle
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fleetio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/fleetio/latest/actions/create-vehicle" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "primaryMeterUnit": "string",
  "vehicleStatusId": 1,
  "vehicleTypeId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fleetio/latest/actions/create-vehicle', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "primaryMeterUnit": "string",
    "vehicleStatusId": 1,
    "vehicleTypeId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | A name to assign to this Vehicle. Must be unique. |
| `primaryMeterUnit` | string | yes | The measurement unit used for the Vehicle's primary, or secondary (if applicable), meter. |
| `vehicleStatusId` | number | yes | The ID of the `Vehicle Status` for this Vehicle. |
| `vehicleTypeId` | number | yes | The ID of the `Vehicle Type` for this Vehicle. |
| `color` | string | no | The color of this Vehicle. |
| `fuelTypeId` | number | no | The ID of the `Fuel Type` associated with this Vehicle. |
| `fuelVolumeUnits` | string | no |  |
| `groupId` | number | no | The id of the `Group` for the vehicle |
| `groupHierarchy` | string | no | A pipe delimited group hierarchy. Ex: "Level 1\|Level 2\|Level 3". Where Level 1 is the parent of Level 2, and 2 is the parent of 3. Any missing nodes in the hierarchy will be created. |
| `labelIds[]` | array<number> | no | The `label_id`(s) of any Labels to assign to this Vehicle. If you wish to keep any existing Labels, those IDs must be included in this array as well. Accepts multiple values as an array. |
| `licensePlate` | string | no | The license plate number of this Vehicle. |
| `make` | string | no | The name of this Vehicle's manufacturer. |
| `model` | string | no | The name of the model of this Vehicle. |
| `ownership` | string | no |  |
| `registrationExpirationMonth` | number | no | The month in which this Vehicle's registration expires. |
| `registrationState` | string | no | The state, province, or territory in which this Vehicle is registered. |
| `secondaryMeter` | boolean | no | Indicates whether or not this Vehicle has a secondary meter. |
| `secondaryMeterUnit` | string | no | The measurement unit used for the Vehicle's primary, or secondary (if applicable), meter. |
| `systemOfMeasurement` | string | no |  |
| `trim` | string | no | The trim level of this Vehicle. |
| `vin` | string | no | The Vehicle Identification Number of this Vehicle. Must be unique. |
| `year` | number | no | This Vehicle's model year. |
| `linkedVehicleIds[]` | array<number> | no | The `vehicle_id`(s) of any Vehicles to link to this Vehicle. Accepts multiple values as an array. |
| `purchaseDetail` | object | no |  |
| `externalIds` | object | no | Any [External IDs](/docs/guides/vehicles/external-vehicle-ids) associated with this Vehicle. |
| `vehicleStatusName` | string | no | The name of the `Vehicle Status` associated with this Vehicle. |
| `vehicleTypeName` | string | no | The name of the `Vehicle Type` associated with this Vehicle. |
| `inServiceDate` | date | no | The date on which this Vehicle was put into service. We recommend using [ISO-8601](/docs/overview/date-formatting) formatted dates to avoid ambiguity. |
| `inServiceMeterValue` | string | no | The meter value at which this Vehicle was put into service. |
| `estimatedServiceMonths` | number | no | The estimated number of months this Vehicle will be in service. |
| `estimatedReplacementMileage` | number | no | The estimated number of miles before which this Vehicle will be replaced. |
| `estimatedResalePrice` | number | no | The estimated resale price of this Vehicle. |
| `outOfServiceDate` | date | no | The date on which this Vehicle was or will be retired. We recommend using [ISO-8601](/docs/overview/date-formatting) formatted dates to avoid ambiguity. |
| `outOfServiceMeterValue` | string | no | The meter value at which this Vehicle was or will be retired. |
| `specs` | object | no |  |
| `customFields` | object | no | *Full details on working with Custom Fields [here](/docs/overview/custom-fields). |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": 1,
      "aiEnabled": true,
      "archivedAt": {},
      "assetableType": "string",
      "axleConfigId": {},
      "color": "string",
      "commentsCount": 1,
      "createdAt": "string",
      "currentLocationEntryId": {},
      "defaultImageUrl": {},
      "defaultImageUrlLarge": {},
      "defaultImageUrlMedium": {},
      "defaultImageUrlSmall": {},
      "documentsCount": 1,
      "documentsIncludingNestedResourcesCount": 1,
      "estimatedReplacementMileage": {},
      "estimatedResalePriceCents": {},
      "estimatedServiceMonths": {},
      "fuelEntriesCount": 1,
      "fuelTypeId": {},
      "fuelTypeName": {},
      "fuelVolumeUnits": "string",
      "groupAncestry": {},
      "groupId": {},
      "groupName": {},
      "id": 1,
      "imagesCount": 1,
      "inServiceDate": {},
      "inServiceMeterValue": {},
      "inspectionSchedulesCount": 1,
      "isSample": true,
      "issuesCount": 1,
      "jobAssignment": {},
      "licensePlate": {},
      "loanAccountNumber": {},
      "loanEndedAt": {},
      "loanInterestRate": {},
      "loanNotes": {},
      "loanStartedAt": {},
      "loanVendorId": {},
      "loanVendorName": {},
      "make": {},
      "model": {},
      "name": "Ava Chen",
      "outOfServiceDate": {},
      "outOfServiceMeterValue": {},
      "ownership": "string",
      "primaryMeterDate": {},
      "primaryMeterUnit": "string",
      "primaryMeterUsagePerDay": {},
      "primaryMeterValue": "string",
      "registrationExpirationMonth": 1,
      "registrationState": {},
      "secondaryMeterDate": {},
      "secondaryMeterUnit": {},
      "secondaryMeterUsagePerDay": {},
      "secondaryMeterValue": "string",
      "serviceEntriesCount": 1,
      "serviceRemindersCount": 1,
      "systemOfMeasurement": "string",
      "trim": {},
      "updatedAt": "string",
      "vehicleRenewalRemindersCount": 1,
      "vehicleStatusColor": "string",
      "vehicleStatusId": 1,
      "vehicleStatusName": "Ava Chen",
      "vehicleTypeId": 1,
      "vehicleTypeName": "Ava Chen",
      "vin": {},
      "warrantiesActiveCount": 1,
      "warrantiesCount": 1,
      "workOrdersCount": 1,
      "year": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | number |  |
| `aiEnabled` | boolean |  |
| `archivedAt` | object |  |
| `assetableType` | string |  |
| `axleConfigId` | object |  |
| `color` | string |  |
| `commentsCount` | number |  |
| `createdAt` | string |  |
| `currentLocationEntryId` | object |  |
| `defaultImageUrl` | object |  |
| `defaultImageUrlLarge` | object |  |
| `defaultImageUrlMedium` | object |  |
| `defaultImageUrlSmall` | object |  |
| `documentsCount` | number |  |
| `documentsIncludingNestedResourcesCount` | number |  |
| `estimatedReplacementMileage` | object |  |
| `estimatedResalePriceCents` | object |  |
| `estimatedServiceMonths` | object |  |
| `fuelEntriesCount` | number |  |
| `fuelTypeId` | object |  |
| `fuelTypeName` | object |  |
| `fuelVolumeUnits` | string |  |
| `groupAncestry` | object |  |
| `groupId` | object |  |
| `groupName` | object |  |
| `id` | number |  |
| `imagesCount` | number |  |
| `inServiceDate` | object |  |
| `inServiceMeterValue` | object |  |
| `inspectionSchedulesCount` | number |  |
| `isSample` | boolean |  |
| `issuesCount` | number |  |
| `jobAssignment` | object |  |
| `licensePlate` | object |  |
| `loanAccountNumber` | object |  |
| `loanEndedAt` | object |  |
| `loanInterestRate` | object |  |
| `loanNotes` | object |  |
| `loanStartedAt` | object |  |
| `loanVendorId` | object |  |
| `loanVendorName` | object |  |
| `make` | object |  |
| `model` | object |  |
| `name` | string |  |
| `outOfServiceDate` | object |  |
| `outOfServiceMeterValue` | object |  |
| `ownership` | string |  |
| `primaryMeterDate` | object |  |
| `primaryMeterUnit` | string |  |
| `primaryMeterUsagePerDay` | object |  |
| `primaryMeterValue` | string |  |
| `registrationExpirationMonth` | number |  |
| `registrationState` | object |  |
| `secondaryMeterDate` | object |  |
| `secondaryMeterUnit` | object |  |
| `secondaryMeterUsagePerDay` | object |  |
| `secondaryMeterValue` | string |  |
| `serviceEntriesCount` | number |  |
| `serviceRemindersCount` | number |  |
| `systemOfMeasurement` | string |  |
| `trim` | object |  |
| `updatedAt` | string |  |
| `vehicleRenewalRemindersCount` | number |  |
| `vehicleStatusColor` | string |  |
| `vehicleStatusId` | number |  |
| `vehicleStatusName` | string |  |
| `vehicleTypeId` | number |  |
| `vehicleTypeName` | string |  |
| `vin` | object |  |
| `warrantiesActiveCount` | number |  |
| `warrantiesCount` | number |  |
| `workOrdersCount` | number |  |
| `year` | object |  |

## Native endpoint

Through the native Fleetio API, this operation is `POST vehicles` (base URL `https://secure.fleetio.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-vehicle.md) for the provider-specific parameters and requirements.

