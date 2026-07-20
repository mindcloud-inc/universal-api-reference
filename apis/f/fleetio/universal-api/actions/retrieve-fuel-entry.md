# Fleetio: Retrieve Fuel Entry

Retrieves a specific fuel entry from Fleetio.

```
GET https://connect.mindcloud.co/v1/universal/fleetio/latest/actions/retrieve-fuel-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fleetio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fleetio/latest/actions/retrieve-fuel-entry?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fleetio/latest/actions/retrieve-fuel-entry?${params}`, {
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
| `id` | string | yes | The id of the relevant record |

## Response

```json
{
  "success": true,
  "data": [
    {
      "commentsCount": 1,
      "costPerHr": {},
      "costPerKm": 1,
      "costPerMi": 1,
      "createdAt": "string",
      "createdBy": {},
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
        "autoVoidedAt": {},
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
      "pricePerVolumeUnit": 1,
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
| `commentsCount` | number |  |
| `costPerHr` | object |  |
| `costPerKm` | number |  |
| `costPerMi` | number |  |
| `createdAt` | string |  |
| `createdBy` | object |  |
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
| `meterEntry.autoVoidedAt` | object |  |
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
| `pricePerVolumeUnit` | number |  |
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

Through the native Fleetio API, this operation is `GET fuel_entries/:id` (base URL `https://secure.fleetio.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-fuel-entry.md) for the provider-specific parameters and requirements.

