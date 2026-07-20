# Fleetio Universal API Examples

These examples use the MindCloud API key and Fleetio connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Vehicles

Retrieves a list of vehicles from Fleetio.

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

Example response:

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

See the full [List Vehicles action reference](actions/list-vehicles.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/fleetio/latest/actions/list-vehicles).

## Create Contact

Creates a new contact in Fleetio.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/fleetio/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "firstName": "Ava"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fleetio/latest/actions/create-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "firstName": "Ava"
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "accountMembershipId": {},
      "archivedAt": {},
      "birthDate": {},
      "city": {},
      "commentsCount": 1,
      "country": {},
      "createdAt": "string",
      "defaultImageUrl": {},
      "documentsCount": 1,
      "email": {},
      "employee": true,
      "employeeNumber": {},
      "firstName": "Ava",
      "groupId": {},
      "groupName": {},
      "homePhoneNumber": {},
      "hourlyLaborRate": {},
      "id": 1,
      "imagesCount": 1,
      "jobTitle": {},
      "lastApiRequest": {},
      "lastMobileAppAccess": {},
      "lastName": {},
      "lastWebAccess": {},
      "leaveDate": {},
      "licenseClass": {},
      "licenseExpiration": {},
      "licenseNumber": {},
      "licenseState": {},
      "middleName": {},
      "mobilePhoneNumber": {},
      "name": "Ava Chen",
      "otherPhoneNumber": {},
      "postalCode": {},
      "region": {},
      "startDate": {},
      "streetAddress": {},
      "streetAddressLine2": {},
      "technician": true,
      "updatedAt": "string",
      "user": {},
      "vehicleOperator": {},
      "workPhoneNumber": {}
    }
  ],
  "meta": {}
}
```

See the full [Create Contact action reference](actions/create-contact.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/fleetio/latest/actions/create-contact).
