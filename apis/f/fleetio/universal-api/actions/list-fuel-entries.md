# Fleetio: List Fuel Entries

Retrieves a list of fuel entries from Fleetio.

```
GET https://connect.mindcloud.co/v1/universal/fleetio/latest/actions/list-fuel-entries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fleetio `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fleetio/latest/actions/list-fuel-entries?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fleetio/latest/actions/list-fuel-entries?${params}`, {
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
      "commentsCount": 1,
      "costPerHr": {},
      "costPerKm": "string",
      "costPerMi": "string",
      "createdAt": "string",
      "date": "string",
      "documentsCount": 1,
      "externalId": {},
      "fuelTypeId": {},
      "id": 1,
      "imagesCount": 1,
      "isSample": true,
      "kpl": "string",
      "liters": "string",
      "litersPerHr": {},
      "lp100k": "string",
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
      "mpgUk": "string",
      "mpgUs": "string",
      "partial": true,
      "personal": true,
      "pricePerVolumeUnit": "string",
      "reference": {},
      "region": {},
      "reset": true,
      "totalAmountCents": 1,
      "ukGallons": "string",
      "ukGallonsPerHr": {},
      "updatedAt": "string",
      "usageInHr": {},
      "usageInKm": "string",
      "usageInMi": "string",
      "usGallons": "string",
      "usGallonsPerHr": {},
      "vehicle": {
        "color": {},
        "defaultImageUrlSmall": "https://example.com",
        "id": 1,
        "licensePlate": {},
        "make": "string",
        "model": "string",
        "name": "Ava Chen",
        "registrationExpirationMonth": 1,
        "registrationState": {},
        "trim": {},
        "vin": "string",
        "year": 1
      },
      "vehicleId": 1,
      "vendorId": {},
      "watchersCount": 1
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
| `costPerKm` | string |  |
| `costPerMi` | string |  |
| `createdAt` | string |  |
| `date` | string |  |
| `documentsCount` | number |  |
| `externalId` | object |  |
| `fuelTypeId` | object |  |
| `id` | number |  |
| `imagesCount` | number |  |
| `isSample` | boolean |  |
| `kpl` | string |  |
| `liters` | string |  |
| `litersPerHr` | object |  |
| `lp100k` | string |  |
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
| `mpgUk` | string |  |
| `mpgUs` | string |  |
| `partial` | boolean |  |
| `personal` | boolean |  |
| `pricePerVolumeUnit` | string |  |
| `reference` | object |  |
| `region` | object |  |
| `reset` | boolean |  |
| `totalAmountCents` | number |  |
| `ukGallons` | string |  |
| `ukGallonsPerHr` | object |  |
| `updatedAt` | string |  |
| `usageInHr` | object |  |
| `usageInKm` | string |  |
| `usageInMi` | string |  |
| `usGallons` | string |  |
| `usGallonsPerHr` | object |  |
| `vehicle.color` | object |  |
| `vehicle.defaultImageUrlSmall` | string |  |
| `vehicle.id` | number |  |
| `vehicle.licensePlate` | object |  |
| `vehicle.make` | string |  |
| `vehicle.model` | string |  |
| `vehicle.name` | string |  |
| `vehicle.registrationExpirationMonth` | number |  |
| `vehicle.registrationState` | object |  |
| `vehicle.trim` | object |  |
| `vehicle.vin` | string |  |
| `vehicle.year` | number |  |
| `vehicleId` | number |  |
| `vendorId` | object |  |
| `watchersCount` | number |  |

## Native endpoint

Through the native Fleetio API, this operation is `GET fuel_entries` (base URL `https://secure.fleetio.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-fuel-entries.md) for the provider-specific parameters and requirements.

