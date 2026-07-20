# Fleetio: Create Fuel Entry

Creates a new fuel entry in Fleetio.

```
POST https://connect.mindcloud.co/v1/universal/fleetio/latest/actions/create-fuel-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fleetio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/fleetio/latest/actions/create-fuel-entry" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "meterEntryAttributes.value": "108043",
  "vehicleId": 1,
  "date": "2026-05-07T12:00:00.000Z",
  "usGallons": 1,
  "meterEntryAttributes": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fleetio/latest/actions/create-fuel-entry', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "meterEntryAttributes.value": "108043",
    "vehicleId": 1,
    "date": "2026-05-07T12:00:00.000Z",
    "usGallons": 1,
    "meterEntryAttributes": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `meterEntryAttributes.value` | number | yes | The actual number on the vehicle's primary meter. Use the current odometer or meter reading for the associated vehicle. Example: `108043`. |
| `vehicleId` | number | yes |  |
| `date` | date | yes | We recommend using [ISO-8601](/docs/overview/date-formatting) formatted dates to avoid ambiguity. |
| `meterEntryAttributes.void` | boolean | no | Set this to true only if Fleetio rejects the meter value as too high or too low and you intentionally want to bypass that validation. |
| `usGallons` | number | yes | The fuel volume amount in US gallons. This field will _only_ be used if the [Vehicle](/docs/api/vehicles) is [configured to use US gallons](https://help.fleetio.com/s/article/Fuel-Settings#vehicle-settings), otherwise it will be ignored. |
| `meterEntryAttributes` | object | yes | Each Fuel Entry requires an associated [Meter Entry](/docs/api/meter-entries) |
| `vendorId` | number | no | The Fleetio `id` of the [Vendor](/docs/api/vendors) associated with this Fuel Entry. |
| `fuelTypeId` | number | no | The Fleetio `id` of the [Fuel Type](/docs/api/fuel-types) associated with this Fuel Entry. |
| `ukGallons` | number | no | The fuel volume amount in UK gallons. This field will _only_ be used if the [Vehicle](/docs/api/vehicles) is [configured to use UK gallons](https://help.fleetio.com/s/article/Fuel-Settings#vehicle-settings), otherwise it will be ignored. |
| `liters` | number | no | The fuel volume amount in liters. This field will be used if the [Vehicle](/docs/api/vehicles) is [configured to use liters](https://help.fleetio.com/s/article/Fuel-Settings#vehicle-settings). |
| `pricePerVolumeUnit` | number | no | The unit price for the Vehicle's [configured volume unit](https://help.fleetio.com/s/article/Fuel-Settings#vehicle-settings). |
| `reference` | string | no | A reference number or identifier for this Fuel Entry. This field is often used to store a receipt number or other unique identifier. |
| `partial` | boolean | no | Indicates whether this Fuel Entry is a partial fill-up. Partial fill-ups are used to record Fuel Entries that are not full fill-ups. This field is `false` if not provided. |
| `personal` | boolean | no | Indicates whether this Fuel Entry is personal. Personal Fuel Entries are used to record fuel purchases that are not associated with a specific Vehicle or Equipment. This field is `false` if not provided. |
| `customFields` | object | no | *Full details on working with Custom Fields [here](/docs/overview/custom-fields). |
| `documentsAttributes[]` | array<object> | no | An array of one or more document objects to add to the record. Follow our [Attaching Documents and Images](/docs/overview/attaching-documents-and-images) guide to upload to our third party storage provider in order to obtain `file_url`. Accepts multiple values as an array. |
| `imagesAttributes[]` | array<object> | no | An array of one or more image objects to add to the record. Follow our [Attaching Documents and Images](/docs/overview/attaching-documents-and-images) guide to upload to our third party storage provider in order to obtain `file_url`. Accepts multiple values as an array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attachmentPermissions": {},
      "commentsCount": 1,
      "costPerHr": {},
      "costPerKm": {},
      "costPerMi": {},
      "createdAt": "string",
      "date": "string",
      "documentsCount": 1,
      "externalId": {},
      "fuelEconomyForCurrentUser": "string",
      "fuelEconomyUnitsForCurrentUser": "string",
      "fuelTypeId": {},
      "fuelTypeName": {},
      "id": 1,
      "imagesCount": 1,
      "isSample": true,
      "kpl": 1,
      "liters": "string",
      "litersPerHr": {},
      "lp100k": 1,
      "mapPreviews": {
        "large": {},
        "largeShort": {},
        "small": {},
        "smallShort": {}
      },
      "meterEntry": {
        "autoVoidedAt": "string",
        "category": {},
        "createdAt": "string",
        "date": "string",
        "id": 1,
        "meterableId": 1,
        "meterableType": "string",
        "meterType": {},
        "type": {},
        "updatedAt": "string",
        "value": "string",
        "vehicleId": 1,
        "void": true
      },
      "mpgUk": 1,
      "mpgUs": 1,
      "partial": true,
      "personal": true,
      "pricePerVolumeUnit": {},
      "rawTransactionData": {},
      "reference": {},
      "region": {},
      "reset": true,
      "totalAmount": 1,
      "ukGallons": "string",
      "ukGallonsPerHr": {},
      "updatedAt": "string",
      "usageInHr": {},
      "usageInKm": "string",
      "usageInMi": "string",
      "usGallons": "string",
      "usGallonsPerHr": {},
      "vehicleId": 1,
      "vehicleName": "Ava Chen",
      "vendorId": {},
      "vendorName": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attachmentPermissions` | object |  |
| `commentsCount` | number |  |
| `costPerHr` | object |  |
| `costPerKm` | object |  |
| `costPerMi` | object |  |
| `createdAt` | string |  |
| `date` | string |  |
| `documentsCount` | number |  |
| `externalId` | object |  |
| `fuelEconomyForCurrentUser` | string |  |
| `fuelEconomyUnitsForCurrentUser` | string |  |
| `fuelTypeId` | object |  |
| `fuelTypeName` | object |  |
| `id` | number |  |
| `imagesCount` | number |  |
| `isSample` | boolean |  |
| `kpl` | number |  |
| `liters` | string |  |
| `litersPerHr` | object |  |
| `lp100k` | number |  |
| `mapPreviews.large` | object |  |
| `mapPreviews.largeShort` | object |  |
| `mapPreviews.small` | object |  |
| `mapPreviews.smallShort` | object |  |
| `meterEntry.autoVoidedAt` | string |  |
| `meterEntry.category` | object |  |
| `meterEntry.createdAt` | string |  |
| `meterEntry.date` | string |  |
| `meterEntry.id` | number |  |
| `meterEntry.meterableId` | number |  |
| `meterEntry.meterableType` | string |  |
| `meterEntry.meterType` | object |  |
| `meterEntry.type` | object |  |
| `meterEntry.updatedAt` | string |  |
| `meterEntry.value` | string |  |
| `meterEntry.vehicleId` | number |  |
| `meterEntry.void` | boolean |  |
| `mpgUk` | number |  |
| `mpgUs` | number |  |
| `partial` | boolean |  |
| `personal` | boolean |  |
| `pricePerVolumeUnit` | object |  |
| `rawTransactionData` | object |  |
| `reference` | object |  |
| `region` | object |  |
| `reset` | boolean |  |
| `totalAmount` | number |  |
| `ukGallons` | string |  |
| `ukGallonsPerHr` | object |  |
| `updatedAt` | string |  |
| `usageInHr` | object |  |
| `usageInKm` | string |  |
| `usageInMi` | string |  |
| `usGallons` | string |  |
| `usGallonsPerHr` | object |  |
| `vehicleId` | number |  |
| `vehicleName` | string |  |
| `vendorId` | object |  |
| `vendorName` | object |  |

## Native endpoint

Through the native Fleetio API, this operation is `POST fuel_entries` (base URL `https://secure.fleetio.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-fuel-entry.md) for the provider-specific parameters and requirements.

