# Fleetio: Retrieve Service Entry

Retrieves a specific service entry from Fleetio.

```
GET https://connect.mindcloud.co/v1/universal/fleetio/latest/actions/retrieve-service-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fleetio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fleetio/latest/actions/retrieve-service-entry?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fleetio/latest/actions/retrieve-service-entry?${params}`, {
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
      "autoIntegrateRepairOrderStatus": "string",
      "autoIntegrateRepairOrderStatusColor": "string",
      "autoIntegrateRoId": 1,
      "autoIntegrateRoLink": {},
      "commentsCount": 1,
      "completedAt": "string",
      "createdAt": "string",
      "date": "string",
      "discount": 1,
      "discountPercentage": 1,
      "discountType": "string",
      "documentsCount": 1,
      "fees": 1,
      "generalNotes": {},
      "id": 1,
      "imagesCount": 1,
      "isSample": true,
      "laborMarkup": 1,
      "laborMarkupPercentage": 1,
      "laborMarkupType": "string",
      "laborSubtotal": 1,
      "laborTimeInSeconds": {},
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
      "partsMarkup": 1,
      "partsMarkupPercentage": 1,
      "partsMarkupType": "string",
      "partsSubtotal": 1,
      "reference": "string",
      "startedAt": "string",
      "status": "string",
      "subtotal": 1,
      "tax1": 1,
      "tax1Percentage": 1,
      "tax1Type": "string",
      "tax2": 1,
      "tax2Percentage": 1,
      "tax2Type": "string",
      "taxFreeLabor": true,
      "totalAmount": 1,
      "updatedAt": "string",
      "vehicleId": 1,
      "vehicleName": "Ava Chen",
      "vendorId": 1,
      "vendorName": "Ava Chen",
      "vmrsRepairPriorityClass": {},
      "warrantyCredits": 1,
      "warrantyCreditsPercentage": 1,
      "warrantyCreditsType": "string",
      "workOrderId": {},
      "workOrderNumber": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `autoIntegrateRepairOrderStatus` | string |  |
| `autoIntegrateRepairOrderStatusColor` | string |  |
| `autoIntegrateRoId` | number |  |
| `autoIntegrateRoLink` | object |  |
| `commentsCount` | number |  |
| `completedAt` | string |  |
| `createdAt` | string |  |
| `date` | string |  |
| `discount` | number |  |
| `discountPercentage` | number |  |
| `discountType` | string |  |
| `documentsCount` | number |  |
| `fees` | number |  |
| `generalNotes` | object |  |
| `id` | number |  |
| `imagesCount` | number |  |
| `isSample` | boolean |  |
| `laborMarkup` | number |  |
| `laborMarkupPercentage` | number |  |
| `laborMarkupType` | string |  |
| `laborSubtotal` | number |  |
| `laborTimeInSeconds` | object |  |
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
| `partsMarkup` | number |  |
| `partsMarkupPercentage` | number |  |
| `partsMarkupType` | string |  |
| `partsSubtotal` | number |  |
| `reference` | string |  |
| `startedAt` | string |  |
| `status` | string |  |
| `subtotal` | number |  |
| `tax1` | number |  |
| `tax1Percentage` | number |  |
| `tax1Type` | string |  |
| `tax2` | number |  |
| `tax2Percentage` | number |  |
| `tax2Type` | string |  |
| `taxFreeLabor` | boolean |  |
| `totalAmount` | number |  |
| `updatedAt` | string |  |
| `vehicleId` | number |  |
| `vehicleName` | string |  |
| `vendorId` | number |  |
| `vendorName` | string |  |
| `vmrsRepairPriorityClass` | object |  |
| `warrantyCredits` | number |  |
| `warrantyCreditsPercentage` | number |  |
| `warrantyCreditsType` | string |  |
| `workOrderId` | object |  |
| `workOrderNumber` | object |  |

## Native endpoint

Through the native Fleetio API, this operation is `GET service_entries/:id` (base URL `https://secure.fleetio.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-service-entry.md) for the provider-specific parameters and requirements.

