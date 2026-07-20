# Fleetio: List Vehicles

Retrieves a list of vehicles from Fleetio.

```
GET https://connect.mindcloud.co/v1/universal/fleetio/latest/actions/list-vehicles
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fleetio `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fleetio/latest/actions/list-vehicles?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fleetio/latest/actions/list-vehicles?${params}`, {
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
      "accountId": 1,
      "aiEnabled": true,
      "archivedAt": {},
      "assetableType": "string",
      "axleConfigId": {},
      "color": {},
      "commentsCount": 1,
      "createdAt": "string",
      "currentLocationEntryId": {},
      "defaultImageUrlSmall": "https://example.com",
      "documentsCount": 1,
      "estimatedReplacementMileage": "string",
      "estimatedResalePriceCents": {},
      "estimatedServiceMonths": 1,
      "fuelEntriesCount": 1,
      "fuelTypeId": {},
      "fuelTypeName": {},
      "fuelVolumeUnits": "string",
      "groupAncestry": "string",
      "groupId": 1,
      "groupName": "Ava Chen",
      "id": 1,
      "imagesCount": 1,
      "inServiceDate": "string",
      "inServiceMeterValue": "string",
      "isSample": true,
      "issuesCount": 1,
      "licensePlate": {},
      "make": "string",
      "model": "string",
      "name": "Ava Chen",
      "outOfServiceDate": "string",
      "outOfServiceMeterValue": "string",
      "ownership": "string",
      "primaryMeterDate": "string",
      "primaryMeterUnit": "string",
      "primaryMeterUsagePerDay": "string",
      "primaryMeterValue": "string",
      "registrationExpirationMonth": 1,
      "registrationState": {},
      "secondaryMeterDate": {},
      "secondaryMeterUnit": {},
      "secondaryMeterUsagePerDay": "string",
      "secondaryMeterValue": "string",
      "serviceEntriesCount": 1,
      "serviceRemindersCount": 1,
      "specs": {
        "accountId": 1,
        "baseTowingCapacity": {},
        "bedLength": {},
        "bodySubtype": "string",
        "bodyType": "string",
        "brakeSystem": "string",
        "cargoVolume": {},
        "createdAt": "string",
        "curbWeight": {},
        "driveType": "string",
        "dutyType": {},
        "engineAspiration": "string",
        "engineBlockType": "string",
        "engineBore": {},
        "engineBoreWithUnits": {},
        "engineBrand": "string",
        "engineCamType": "string",
        "engineCompression": {},
        "engineCylinders": 1,
        "engineDescription": "string",
        "engineDisplacement": 1,
        "engineStroke": {},
        "engineValves": {},
        "epaCity": {},
        "epaCombined": {},
        "epaHighway": {},
        "frontTirePsi": {},
        "frontTireType": {},
        "frontTrackWidth": {},
        "frontWheelDiameter": {},
        "fuelInduction": "string",
        "fuelQuality": {},
        "fuelTank2Capacity": {},
        "fuelTankCapacity": {},
        "grossVehicleWeightRating": {},
        "groundClearance": {},
        "height": {},
        "id": 1,
        "interiorVolume": {},
        "length": {},
        "maxHp": 1,
        "maxPayload": {},
        "maxTorque": 1,
        "msrp": {},
        "msrpCents": {},
        "oilCapacity": {},
        "passengerVolume": {},
        "rearAxleType": {},
        "rearTirePsi": {},
        "rearTireType": {},
        "rearTrackWidth": {},
        "rearWheelDiameter": {},
        "redlineRpm": {},
        "transmissionBrand": {},
        "transmissionDescription": {},
        "transmissionGears": {},
        "transmissionType": {},
        "updatedAt": "string",
        "vehicleId": 1,
        "weightClass": {},
        "wheelbase": {},
        "wheelbaseWithUnits": {},
        "width": {}
      },
      "systemOfMeasurement": "string",
      "trim": {},
      "updatedAt": "string",
      "vehicleRenewalRemindersCount": 1,
      "vehicleStatusColor": "string",
      "vehicleStatusId": 1,
      "vehicleStatusName": "Ava Chen",
      "vehicleTypeId": 1,
      "vehicleTypeName": "Ava Chen",
      "vin": "string",
      "workOrdersCount": 1,
      "year": 1
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
| `color` | object |  |
| `commentsCount` | number |  |
| `createdAt` | string |  |
| `currentLocationEntryId` | object |  |
| `defaultImageUrlSmall` | string |  |
| `documentsCount` | number |  |
| `estimatedReplacementMileage` | string |  |
| `estimatedResalePriceCents` | object |  |
| `estimatedServiceMonths` | number |  |
| `fuelEntriesCount` | number |  |
| `fuelTypeId` | object |  |
| `fuelTypeName` | object |  |
| `fuelVolumeUnits` | string |  |
| `groupAncestry` | string |  |
| `groupId` | number |  |
| `groupName` | string |  |
| `id` | number |  |
| `imagesCount` | number |  |
| `inServiceDate` | string |  |
| `inServiceMeterValue` | string |  |
| `isSample` | boolean |  |
| `issuesCount` | number |  |
| `licensePlate` | object |  |
| `make` | string |  |
| `model` | string |  |
| `name` | string |  |
| `outOfServiceDate` | string |  |
| `outOfServiceMeterValue` | string |  |
| `ownership` | string |  |
| `primaryMeterDate` | string |  |
| `primaryMeterUnit` | string |  |
| `primaryMeterUsagePerDay` | string |  |
| `primaryMeterValue` | string |  |
| `registrationExpirationMonth` | number |  |
| `registrationState` | object |  |
| `secondaryMeterDate` | object |  |
| `secondaryMeterUnit` | object |  |
| `secondaryMeterUsagePerDay` | string |  |
| `secondaryMeterValue` | string |  |
| `serviceEntriesCount` | number |  |
| `serviceRemindersCount` | number |  |
| `specs.accountId` | number |  |
| `specs.baseTowingCapacity` | object |  |
| `specs.bedLength` | object |  |
| `specs.bodySubtype` | string |  |
| `specs.bodyType` | string |  |
| `specs.brakeSystem` | string |  |
| `specs.cargoVolume` | object |  |
| `specs.createdAt` | string |  |
| `specs.curbWeight` | object |  |
| `specs.driveType` | string |  |
| `specs.dutyType` | object |  |
| `specs.engineAspiration` | string |  |
| `specs.engineBlockType` | string |  |
| `specs.engineBore` | object |  |
| `specs.engineBoreWithUnits` | object |  |
| `specs.engineBrand` | string |  |
| `specs.engineCamType` | string |  |
| `specs.engineCompression` | object |  |
| `specs.engineCylinders` | number |  |
| `specs.engineDescription` | string |  |
| `specs.engineDisplacement` | number |  |
| `specs.engineStroke` | object |  |
| `specs.engineValves` | object |  |
| `specs.epaCity` | object |  |
| `specs.epaCombined` | object |  |
| `specs.epaHighway` | object |  |
| `specs.frontTirePsi` | object |  |
| `specs.frontTireType` | object |  |
| `specs.frontTrackWidth` | object |  |
| `specs.frontWheelDiameter` | object |  |
| `specs.fuelInduction` | string |  |
| `specs.fuelQuality` | object |  |
| `specs.fuelTank2Capacity` | object |  |
| `specs.fuelTankCapacity` | object |  |
| `specs.grossVehicleWeightRating` | object |  |
| `specs.groundClearance` | object |  |
| `specs.height` | object |  |
| `specs.id` | number |  |
| `specs.interiorVolume` | object |  |
| `specs.length` | object |  |
| `specs.maxHp` | number |  |
| `specs.maxPayload` | object |  |
| `specs.maxTorque` | number |  |
| `specs.msrp` | object |  |
| `specs.msrpCents` | object |  |
| `specs.oilCapacity` | object |  |
| `specs.passengerVolume` | object |  |
| `specs.rearAxleType` | object |  |
| `specs.rearTirePsi` | object |  |
| `specs.rearTireType` | object |  |
| `specs.rearTrackWidth` | object |  |
| `specs.rearWheelDiameter` | object |  |
| `specs.redlineRpm` | object |  |
| `specs.transmissionBrand` | object |  |
| `specs.transmissionDescription` | object |  |
| `specs.transmissionGears` | object |  |
| `specs.transmissionType` | object |  |
| `specs.updatedAt` | string |  |
| `specs.vehicleId` | number |  |
| `specs.weightClass` | object |  |
| `specs.wheelbase` | object |  |
| `specs.wheelbaseWithUnits` | object |  |
| `specs.width` | object |  |
| `systemOfMeasurement` | string |  |
| `trim` | object |  |
| `updatedAt` | string |  |
| `vehicleRenewalRemindersCount` | number |  |
| `vehicleStatusColor` | string |  |
| `vehicleStatusId` | number |  |
| `vehicleStatusName` | string |  |
| `vehicleTypeId` | number |  |
| `vehicleTypeName` | string |  |
| `vin` | string |  |
| `workOrdersCount` | number |  |
| `year` | number |  |

## Native endpoint

Through the native Fleetio API, this operation is `GET vehicles` (base URL `https://secure.fleetio.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-vehicles.md) for the provider-specific parameters and requirements.

