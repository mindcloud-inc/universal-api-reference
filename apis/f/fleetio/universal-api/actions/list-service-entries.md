# Fleetio: List Service Entries

Retrieves a list of service entries from Fleetio.

```
GET https://connect.mindcloud.co/v1/universal/fleetio/latest/actions/list-service-entries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fleetio `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fleetio/latest/actions/list-service-entries?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fleetio/latest/actions/list-service-entries?${params}`, {
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
      "autoIntegrateRepairOrderStatus": {},
      "commentsCount": 1,
      "completedAt": "string",
      "createdAt": "string",
      "discountCents": 1,
      "discountPercentage": "string",
      "discountType": "string",
      "documentsCount": 1,
      "feesCents": 1,
      "generalNotes": {},
      "id": 1,
      "imagesCount": 1,
      "isSample": true,
      "laborSubtotalCents": 1,
      "laborTimeInSeconds": {},
      "partsSubtotalCents": 1,
      "primaryMeterEntry": {
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
      "reference": {},
      "startedAt": {},
      "status": "string",
      "subtotalCents": 1,
      "tax1Cents": 1,
      "tax1Percentage": "string",
      "tax1Type": "string",
      "tax2Cents": 1,
      "tax2Percentage": "string",
      "tax2Type": "string",
      "totalAmountCents": 1,
      "updatedAt": "string",
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
      "vendor": {
        "city": "string",
        "country": "string",
        "externalId": {},
        "id": 1,
        "name": "Ava Chen",
        "phone": "string",
        "postalCode": "string",
        "region": "string"
      },
      "vendorId": {},
      "vendorName": {},
      "warrantyCreditsCents": 1,
      "warrantyCreditsPercentage": "string",
      "warrantyCreditsType": "string",
      "workOrderId": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `autoIntegrateRepairOrderStatus` | object |  |
| `commentsCount` | number |  |
| `completedAt` | string |  |
| `createdAt` | string |  |
| `discountCents` | number |  |
| `discountPercentage` | string |  |
| `discountType` | string |  |
| `documentsCount` | number |  |
| `feesCents` | number |  |
| `generalNotes` | object |  |
| `id` | number |  |
| `imagesCount` | number |  |
| `isSample` | boolean |  |
| `laborSubtotalCents` | number |  |
| `laborTimeInSeconds` | object |  |
| `partsSubtotalCents` | number |  |
| `primaryMeterEntry.autoVoidedAt` | object |  |
| `primaryMeterEntry.category` | object |  |
| `primaryMeterEntry.createdAt` | string |  |
| `primaryMeterEntry.date` | string |  |
| `primaryMeterEntry.id` | number |  |
| `primaryMeterEntry.meterableId` | number |  |
| `primaryMeterEntry.meterableType` | string |  |
| `primaryMeterEntry.meterType` | object |  |
| `primaryMeterEntry.type` | object |  |
| `primaryMeterEntry.updatedAt` | string |  |
| `primaryMeterEntry.value` | string |  |
| `primaryMeterEntry.vehicleId` | number |  |
| `primaryMeterEntry.void` | boolean |  |
| `reference` | object |  |
| `startedAt` | object |  |
| `status` | string |  |
| `subtotalCents` | number |  |
| `tax1Cents` | number |  |
| `tax1Percentage` | string |  |
| `tax1Type` | string |  |
| `tax2Cents` | number |  |
| `tax2Percentage` | string |  |
| `tax2Type` | string |  |
| `totalAmountCents` | number |  |
| `updatedAt` | string |  |
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
| `vendor.city` | string |  |
| `vendor.country` | string |  |
| `vendor.externalId` | object |  |
| `vendor.id` | number |  |
| `vendor.name` | string |  |
| `vendor.phone` | string |  |
| `vendor.postalCode` | string |  |
| `vendor.region` | string |  |
| `vendorId` | object |  |
| `vendorName` | object |  |
| `warrantyCreditsCents` | number |  |
| `warrantyCreditsPercentage` | string |  |
| `warrantyCreditsType` | string |  |
| `workOrderId` | object |  |

## Native endpoint

Through the native Fleetio API, this operation is `GET service_entries` (base URL `https://secure.fleetio.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-service-entries.md) for the provider-specific parameters and requirements.

