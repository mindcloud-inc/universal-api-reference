# Fleetio: Update Work Order

Updates an existing work order in Fleetio.

```
PUT https://connect.mindcloud.co/v1/universal/fleetio/latest/actions/update-work-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fleetio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/fleetio/latest/actions/update-work-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fleetio/latest/actions/update-work-order', {
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
| `id` | string | yes | The id of the relevant record |
| `issuedAt` | date | no | The date and time at which this Work Order was issued. We recommend using [ISO-8601](/docs/overview/date-formatting) formatted dates to avoid ambiguity. |
| `startedAt` | date | no | The date and time at which this Work Order was started. We recommend using [ISO-8601](/docs/overview/date-formatting) formatted dates to avoid ambiguity. |
| `completedAt` | date | no | The date and time at which this Work Order was completed. We recommend using [ISO-8601](/docs/overview/date-formatting) formatted dates to avoid ambiguity. |
| `workOrderStatusId` | number | no |  |
| `invoiceNumber` | string | no | The number of the `Invoice` associated with this Work Order. |
| `vendorId` | number | no |  |
| `vendorName` | string | no | The name of the `Vendor` associated with this Work Order. |
| `vehicleId` | number | no |  |
| `vehicleName` | string | no | The name of the `Vehicle` associated with this Work Order. |
| `discountType` | string | no | The type of discount applied to this Work Order. |
| `discount` | number | no | The discount amount in decimal currency units applied to this Work Order. |
| `discountPercentage` | number | no | The percentage of the discount applied to this Work Order. Used if `discount_type` is set to `percentage`. |
| `partsMarkupPercentage` | number | no | The percentage of the parts markup applied to this Work Order. Used if `parts_markup_type` is set to `percentage`. Note: Parts markup fields are only writiable for Premium tier Fleetio Plan. |
| `partsMarkupType` | string | no | The type of parts markup to apply to this record. Note: Parts markup fields are only writiable for Premium tier Fleetio Plan. |
| `partsMarkup` | number | no | The amount of the parts markup applied to this Work Order. Used if `parts_markup_type` is set to `fixed`. Note: Parts markup fields are only writiable for Premium tier Fleetio Plan. |
| `laborMarkupPercentage` | number | no | The percentage of the labor markup applied to this Work Order. Used if `labor_markup_type` is set to `percentage`. Note: Labor markup fields are only writiable for Premium tier Fleetio Plan. |
| `laborMarkupType` | string | no | The type of labor markup to apply to this record. Note: Labor markup fields are only writiable for Premium tier Fleetio Plan. |
| `laborMarkup` | number | no | The amount of the labor markup applied to this Work Order. Used if `labor_markup_type` is set to `fixed`. Note: Labor markup fields are only writiable for Premium tier Fleetio Plan. |
| `tax1Percentage` | number | no | The percentage of the first tax applied to this Work Order. Used if `tax_1_type` is set to `percentage`. |
| `tax1Type` | string | no | The type of tax to apply to this record. |
| `tax1` | number | no | The amount of the first tax applied to this Work Order. Used if `tax_1_type` is set to `amount`. |
| `tax2Percentage` | number | no | The percentage of the second tax applied to this Work Order. Used if `tax_2_type` is set to `percentage`. |
| `tax2Type` | string | no | The type of tax to apply to this record. |
| `tax2` | number | no | The amount of the second tax applied to this Work Order. Used if `tax_2_type` is set to `amount`. |
| `issuedById` | number | no |  |
| `contactId` | number | no |  |
| `labelList` | string | no | A comma separated list of tags associated with this record. The only delimiter allowed is a comma (`,`). Please remove any commas from your labels before saving the record. |
| `purchaseOrderNumber` | string | no | The number of the `Purchase Order` associated with this Work Order. |
| `description` | string | no | A description of this Work Order. |
| `number` | number | no | The number to be applied to this Work Order. Must be unique. |
| `meterEntryAttributes` | object | no | A Work Order may also be associated with a [Meter Entry](/docs/api/meter-entries). |
| `secondaryMeterEntryAttributes` | object | no | A Work Order may also be associated with a secondary [Meter Entry](/docs/api/meter-entries). |
| `startingMeterEntryAttributes` | object | no | The meter reading at the start of this Work Order. |
| `endingMeterEntryAttributes` | object | no | The meter reading at the end of this Work Order. |
| `startingSecondaryMeterEntryAttributes` | object | no | The secondary meter reading at the start of this Work Order. |
| `endingSecondaryMeterEntryAttributes` | object | no | The secondary meter reading at the end of this Work Order. |
| `customFields` | object | no | *Full details on working with Custom Fields [here](/docs/overview/custom-fields). |
| `endingMeterSameAsStart` | boolean | no | Use start meter for completion meter? |
| `vmrsRepairPriorityClassId` | number | no |  |
| `scheduledAt` | date | no | The date and time at which this Work Order is scheduled. We recommend using [ISO-8601](/docs/overview/date-formatting) formatted dates to avoid ambiguity. |
| `expectedCompletedAt` | date | no | The date and time at which this Work Order is expected to be completed. We recommend using [ISO-8601](/docs/overview/date-formatting) formatted dates to avoid ambiguity. |
| `commentsAttributes` | array<object> | no | A list of `Comments` to be added to this Work Order. |
| `workOrderLineItemsAttributes` | array<object> | no | A list of `Work Order Line Items` to be added to this Work Order. |
| `workOrderSubLineItemsAttributes` | array<object> | no | A list of `Work Order Sub Line Items` to be added to this Work Order. |
| `issueIds` | array<number> | no | A list of `Issues` to be added to this Work Order. |
| `labelIds` | array<number> | no | A list of `Labels` to be added to this Work Order. |
| `documentsAttributes` | array<object> | no | An array of one or more document objects to add to the record. Follow our [Attaching Documents and Images](/docs/overview/attaching-documents-and-images) guide to upload to our third party storage provider in order to obtain `file_url`. |
| `imagesAttributes` | array<object> | no | An array of one or more image objects to add to the record. Follow our [Attaching Documents and Images](/docs/overview/attaching-documents-and-images) guide to upload to our third party storage provider in order to obtain `file_url`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attachmentPermissions": {},
      "commentsCount": 1,
      "completedAt": {},
      "contactId": {},
      "contactName": {},
      "createdAt": "string",
      "createdById": 1,
      "description": {},
      "discount": 1,
      "discountPercentage": 1,
      "discountType": "string",
      "documentsCount": 1,
      "durationInSeconds": {},
      "endingMeterSameAsStart": true,
      "expectedCompletedAt": {},
      "id": 1,
      "imagesCount": 1,
      "invoiceNumber": "string",
      "issuedAt": "string",
      "issuedById": 1,
      "issuedByName": "Ava Chen",
      "isWatched": true,
      "laborMarkup": 1,
      "laborMarkupPercentage": 1,
      "laborMarkupType": "string",
      "laborSubtotal": 1,
      "laborTimeInSeconds": {},
      "number": "string",
      "partsMarkup": 1,
      "partsMarkupPercentage": 1,
      "partsMarkupType": "string",
      "partsSubtotal": 1,
      "purchaseOrderNumber": {},
      "scheduledAt": {},
      "selectedPartWarrantyOpportunitiesCount": 1,
      "startedAt": {},
      "state": "string",
      "subtotal": 1,
      "tax1": 1,
      "tax1Percentage": 1,
      "tax1Type": "string",
      "tax2": 1,
      "tax2Percentage": 1,
      "tax2Type": "string",
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
      "watchersCount": 1,
      "workOrderStatusColor": "string",
      "workOrderStatusId": 1,
      "workOrderStatusName": "Ava Chen"
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
| `completedAt` | object |  |
| `contactId` | object |  |
| `contactName` | object |  |
| `createdAt` | string |  |
| `createdById` | number |  |
| `description` | object |  |
| `discount` | number |  |
| `discountPercentage` | number |  |
| `discountType` | string |  |
| `documentsCount` | number |  |
| `durationInSeconds` | object |  |
| `endingMeterSameAsStart` | boolean |  |
| `expectedCompletedAt` | object |  |
| `id` | number |  |
| `imagesCount` | number |  |
| `invoiceNumber` | string |  |
| `issuedAt` | string |  |
| `issuedById` | number |  |
| `issuedByName` | string |  |
| `isWatched` | boolean |  |
| `laborMarkup` | number |  |
| `laborMarkupPercentage` | number |  |
| `laborMarkupType` | string |  |
| `laborSubtotal` | number |  |
| `laborTimeInSeconds` | object |  |
| `number` | string |  |
| `partsMarkup` | number |  |
| `partsMarkupPercentage` | number |  |
| `partsMarkupType` | string |  |
| `partsSubtotal` | number |  |
| `purchaseOrderNumber` | object |  |
| `scheduledAt` | object |  |
| `selectedPartWarrantyOpportunitiesCount` | number |  |
| `startedAt` | object |  |
| `state` | string |  |
| `subtotal` | number |  |
| `tax1` | number |  |
| `tax1Percentage` | number |  |
| `tax1Type` | string |  |
| `tax2` | number |  |
| `tax2Percentage` | number |  |
| `tax2Type` | string |  |
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
| `watchersCount` | number |  |
| `workOrderStatusColor` | string |  |
| `workOrderStatusId` | number |  |
| `workOrderStatusName` | string |  |

## Native endpoint

Through the native Fleetio API, this operation is `PATCH work_orders/:id` (base URL `https://secure.fleetio.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-work-order.md) for the provider-specific parameters and requirements.

