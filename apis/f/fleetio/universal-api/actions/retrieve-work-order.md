# Fleetio: Retrieve Work Order

Retrieves a specific work order from Fleetio.

```
GET https://connect.mindcloud.co/v1/universal/fleetio/latest/actions/retrieve-work-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fleetio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fleetio/latest/actions/retrieve-work-order?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fleetio/latest/actions/retrieve-work-order?${params}`, {
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
      "invoiceNumber": {},
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
      "vendorId": {},
      "vendorName": {},
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
| `invoiceNumber` | object |  |
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
| `vendorId` | object |  |
| `vendorName` | object |  |
| `vmrsRepairPriorityClass` | object |  |
| `warrantyCredits` | number |  |
| `warrantyCreditsPercentage` | number |  |
| `warrantyCreditsType` | string |  |
| `watchersCount` | number |  |
| `workOrderStatusColor` | string |  |
| `workOrderStatusId` | number |  |
| `workOrderStatusName` | string |  |

## Native endpoint

Through the native Fleetio API, this operation is `GET work_orders/:id` (base URL `https://secure.fleetio.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-work-order.md) for the provider-specific parameters and requirements.

