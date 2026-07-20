# Fleetio: Create Service Entry

Creates a new service entry in Fleetio.

```
POST https://connect.mindcloud.co/v1/universal/fleetio/latest/actions/create-service-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fleetio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/fleetio/latest/actions/create-service-entry" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "completedAt": "2026-05-07T12:00:00.000Z",
  "meterEntryAttributes.value": "20812",
  "vehicleId": 1,
  "meterEntryAttributes": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fleetio/latest/actions/create-service-entry', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "completedAt": "2026-05-07T12:00:00.000Z",
    "meterEntryAttributes.value": "20812",
    "vehicleId": 1,
    "meterEntryAttributes": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `completedAt` | date | yes | The date and time at which the Service Entry was completed. We recommend using [ISO-8601](/docs/overview/date-formatting) formatted dates to avoid ambiguity. |
| `meterEntryAttributes.value` | number | yes | The actual number on the vehicle's primary meter. Use the current odometer or meter reading for the associated vehicle. Example: `20812`. |
| `meterEntryAttributes.void` | boolean | no | Set this to true only if Fleetio rejects the meter value as too high or too low and you intentionally want to bypass that validation. |
| `vehicleId` | number | yes |  |
| `meterEntryAttributes` | object | yes | A Service Entry may be associated with a [Meter Entry](/docs/api/meter-entries) |
| `startedAt` | date | no | The date and time at which the Service Entry was started. We recommend using [ISO-8601](/docs/overview/date-formatting) formatted dates to avoid ambiguity. |
| `vehicleVin` | string | no | The VIN of the `Vehicle` associated with this Service Entry. |
| `vendorId` | number | no |  |
| `reference` | string | no | A reference number for this Service Entry. |
| `labelList` | string | no | A comma separated list of tags associated with this record. The only delimiter allowed is a comma (`,`). Please remove any commas from your labels before saving the record. |
| `generalNotes` | string | no | Any general notes about this Service Entry. |
| `vmrsRepairPriorityClassId` | number | no |  |
| `customFields` | object | no | *Full details on working with Custom Fields [here](/docs/overview/custom-fields). |
| `secondaryMeterEntryAttributes` | object | no | A Service Entry may also be associated with a secondary [Meter Entry](/docs/api/meter-entries) |
| `serviceEntryLineItemsAttributes[]` | array<object> | no | Accepts multiple values as an array. |
| `issueIds[]` | array<number> | no | The IDs of any Issues associated with this Service Entry. Accepts multiple values as an array. |
| `serviceTaskIds[]` | array<number> | no | The IDs of any Service Tasks associated with this Service Entry. Accepts multiple values as an array. |
| `commentsAttributes[]` | array<object> | no | Accepts multiple values as an array. |
| `documentsAttributes[]` | array<object> | no | An array of one or more document objects to add to the record. Follow our [Attaching Documents and Images](/docs/overview/attaching-documents-and-images) guide to upload to our third party storage provider in order to obtain `file_url`. Accepts multiple values as an array. |
| `imagesAttributes[]` | array<object> | no | An array of one or more image objects to add to the record. Follow our [Attaching Documents and Images](/docs/overview/attaching-documents-and-images) guide to upload to our third party storage provider in order to obtain `file_url`. Accepts multiple values as an array. |
| `laborSubtotal` | number | no | The total cost of labor for this Service Entry. This is calculated by summing the `labor_cost` of each `Service Entry Line Item`. |
| `partsSubtotal` | number | no | The total cost of `Parts` for this Service Entry. This is calculated by summing the `parts_cost` of each `Service Entry Line Item`. |
| `subtotal` | number | no | The subtotal amount of this Service Entry before any discounts or taxes. This is calculated by summing the `subtotal` of each `Service Entry Line Item`. |
| `discount` | number | no | The total discount amount for this Service Entry. |
| `discountPercentage` | number | no | The total discount percentage for this Service Entry. |
| `discountType` | string | no | The type of discount applied to this record. |
| `tax1` | number | no | The first tax amount for this Service Entry. |
| `tax1Percentage` | number | no | The first tax percentage for this Service Entry. |
| `tax1Type` | string | no | The type of tax to apply to this record. |
| `tax2` | number | no | The second tax amount for this Service Entry. |
| `tax2Percentage` | number | no | The second tax percentage for this Service Entry. |
| `tax2Type` | string | no | The type of tax to apply to this record. |
| `totalAmount` | number | no | The grand total of this Service Entry. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attachmentPermissions": {},
      "autoIntegrateRepairOrderStatus": {},
      "autoIntegrateRepairOrderStatusColor": "string",
      "autoIntegrateRoId": {},
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
      "reference": {},
      "startedAt": {},
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
      "vendorId": {},
      "vendorName": {},
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
| `attachmentPermissions` | object |  |
| `autoIntegrateRepairOrderStatus` | object |  |
| `autoIntegrateRepairOrderStatusColor` | string |  |
| `autoIntegrateRoId` | object |  |
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
| `reference` | object |  |
| `startedAt` | object |  |
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
| `vendorId` | object |  |
| `vendorName` | object |  |
| `vmrsRepairPriorityClass` | object |  |
| `warrantyCredits` | number |  |
| `warrantyCreditsPercentage` | number |  |
| `warrantyCreditsType` | string |  |
| `workOrderId` | object |  |
| `workOrderNumber` | object |  |

## Native endpoint

Through the native Fleetio API, this operation is `POST service_entries` (base URL `https://secure.fleetio.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-service-entry.md) for the provider-specific parameters and requirements.

