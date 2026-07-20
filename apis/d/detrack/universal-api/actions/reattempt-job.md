# Detrack: Reattempt Job

Reattempts a failed job in Detrack.

```
PUT https://connect.mindcloud.co/v1/universal/detrack/latest/actions/reattempt-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Detrack `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/detrack/latest/actions/reattempt-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "data": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/detrack/latest/actions/reattempt-job', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "data": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `data` | object | yes | Body object sent as data with do_number and date for the job to reattempt. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountNumber": {},
      "actualCrates": {},
      "actualPallets": {},
      "actualUtilization": {},
      "actualWeight": {},
      "address": "string",
      "address1": {},
      "address2": {},
      "address3": {},
      "addressLat": {},
      "addressLng": {},
      "addressTrackedAt": {},
      "arrivedAddress": {},
      "arrivedAt": {},
      "arrivedLat": {},
      "arrivedLng": {},
      "assignTo": {},
      "attachmentUrl": {},
      "attempt": 1,
      "autoReschedule": {},
      "bankPrefix": {},
      "billingAddress": {},
      "bins": {},
      "boxes": {},
      "bundles": {},
      "calledAt": {},
      "canReattempt": true,
      "carrier": {},
      "cartons": {},
      "city": {},
      "companyName": {},
      "completionDate": {},
      "connectHost": {},
      "connectId": {},
      "connectToken": {},
      "contactlessSignatureLink": "https://example.com",
      "contractorGroupName": "Ava Chen",
      "country": {},
      "createdAt": "string",
      "cubicMeter": {},
      "cubicMeters": {},
      "customer": {},
      "customerFeedback": {},
      "date": "string",
      "deliverToCollectFrom": "string",
      "department": {},
      "depot": {},
      "depotAddress": {},
      "depotContact": {},
      "depotContactNo": {},
      "destinationTimeWindow": {},
      "detrackNumber": "string",
      "doNumber": "string",
      "door": {},
      "driverMobileNumber": {},
      "driverRating": {},
      "envelopes": {},
      "etaTime": {},
      "faxNumber": {},
      "geofenceAckAt": {},
      "geofenceAckLat": {},
      "geofenceAckLng": {},
      "goodsServiceRating": {},
      "groupCode": {},
      "groupId": {},
      "groupName": {},
      "headToDeliveryAt": {},
      "holdTime": {},
      "id": "string",
      "identificationNumber": {},
      "instructions": {},
      "insuranceCoverage": true,
      "insurancePrice": {},
      "invoiceAmount": {},
      "invoiceNumber": {},
      "items": [
        {
          "actualQuantity": {},
          "batchNumber": {},
          "checked": true,
          "comments": {},
          "description": {},
          "expiryDate": {},
          "fixedPrice": {},
          "followUpQuantity": {},
          "followUpReason": {},
          "id": "string",
          "inboundQuantity": {},
          "minimumQuantity": {},
          "photoUrl": {},
          "purchaseOrderNumber": {},
          "quantity": {},
          "rejectQuantity": 1,
          "rejectReason": {},
          "reworkQuantity": {},
          "reworkReason": {},
          "serialNumbers": "string",
          "sku": {},
          "unitOfMeasure": {},
          "unitPrice": {},
          "unloadTimeActual": {},
          "unloadTimeEstimate": {},
          "weight": {}
        }
      ],
      "itemsCount": 1,
      "jobAge": 1,
      "jobFee": {},
      "jobOrder": {},
      "jobOwner": {},
      "jobPrice": {},
      "jobReceivedDate": {},
      "jobReleaseTime": {},
      "jobSequence": {},
      "jobTime": {},
      "jobType": {},
      "lastName": {},
      "liveEta": {},
      "lockerAddress": {},
      "lockerError": {},
      "lockerLat": {},
      "lockerLng": {},
      "lockerStationId": {},
      "lockerTransactionId": {},
      "lockerTransactionStatus": {},
      "marketplaceOffer": {},
      "massPod": {},
      "milestones": [
        {
          "assignTo": "string",
          "createdAt": "string",
          "podAt": "string",
          "reason": {},
          "status": "string",
          "userName": "Ava Chen"
        }
      ],
      "note": {},
      "notifyEmail": {},
      "numberOfShippingLabels": {},
      "onDemand": true,
      "openToMarketplace": {},
      "orderNumber": {},
      "otherPhoneNumbers": {},
      "pallets": {},
      "parcelHeight": {},
      "parcelLength": {},
      "parcelWidth": {},
      "payerType": {},
      "paymentAmount": {},
      "paymentCollected": {},
      "paymentMode": {},
      "phoneNumber": {},
      "photo10At": {},
      "photo10FileUrl": {},
      "photo1At": {},
      "photo1FileUrl": {},
      "photo2At": {},
      "photo2FileUrl": {},
      "photo3At": {},
      "photo3FileUrl": {},
      "photo4At": {},
      "photo4FileUrl": {},
      "photo5At": {},
      "photo5FileUrl": {},
      "photo6At": {},
      "photo6FileUrl": {},
      "photo7At": {},
      "photo7FileUrl": {},
      "photo8At": {},
      "photo8FileUrl": {},
      "photo9At": {},
      "photo9FileUrl": {},
      "photoPreviewAckAt": {},
      "photoPreviewAckLat": {},
      "photoPreviewAckLng": {},
      "pickUpPhotoPreviewAckAt": {},
      "pickUpPhotoPreviewAckLat": {},
      "pickUpPhotoPreviewAckLng": {},
      "pieces": {},
      "podAddress": "string",
      "podAt": {},
      "podGpsPermission": {},
      "podGpsStatus": {},
      "podLat": "string",
      "podLng": "string",
      "podTime": {},
      "postalCode": {},
      "primaryJobStatus": "string",
      "priority": {},
      "rateCardChargeable": {},
      "rateCardChargeableId": {},
      "rateCardId": {},
      "rateCardVersion": {},
      "reason": {},
      "reattempted": {},
      "receivedBySentBy": {},
      "recipientSenderDevicePodAt": {},
      "recipientSenderDeviceSignatureFileUrl": {},
      "recipientSenderDeviceSignedBy": {},
      "remarks": {},
      "rolls": {},
      "runNumber": {},
      "salesPerson": {},
      "senderPhoneNumber": {},
      "serialNumber": {},
      "serviceTime": {},
      "serviceType": {},
      "signatureFileUrl": {},
      "signedAt": {},
      "source": {},
      "startDate": "string",
      "state": {},
      "status": "string",
      "temperature": {},
      "textedAt": {},
      "timeWindow": {},
      "timeWindowFrom": {},
      "timeWindowTo": {},
      "timeZone": {},
      "totalPrice": {},
      "trackingLink": "https://example.com",
      "trackingNumber": {},
      "trackingStatus": "string",
      "trackingStatusCode": "string",
      "trays": {},
      "type": "string",
      "updatedAt": "string",
      "useLocker": true,
      "vehicleType": {},
      "verificationCode": 1,
      "warehouseAddress": {},
      "webhookUrl": {},
      "weight": {},
      "zone": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountNumber` | object |  |
| `actualCrates` | object |  |
| `actualPallets` | object |  |
| `actualUtilization` | object |  |
| `actualWeight` | object |  |
| `address` | string |  |
| `address1` | object |  |
| `address2` | object |  |
| `address3` | object |  |
| `addressLat` | object |  |
| `addressLng` | object |  |
| `addressTrackedAt` | object |  |
| `arrivedAddress` | object |  |
| `arrivedAt` | object |  |
| `arrivedLat` | object |  |
| `arrivedLng` | object |  |
| `assignTo` | object |  |
| `attachmentUrl` | object |  |
| `attempt` | number |  |
| `autoReschedule` | object |  |
| `bankPrefix` | object |  |
| `billingAddress` | object |  |
| `bins` | object |  |
| `boxes` | object |  |
| `bundles` | object |  |
| `calledAt` | object |  |
| `canReattempt` | boolean |  |
| `carrier` | object |  |
| `cartons` | object |  |
| `city` | object |  |
| `companyName` | object |  |
| `completionDate` | object |  |
| `connectHost` | object |  |
| `connectId` | object |  |
| `connectToken` | object |  |
| `contactlessSignatureLink` | string |  |
| `contractorGroupName` | string |  |
| `country` | object |  |
| `createdAt` | string |  |
| `cubicMeter` | object |  |
| `cubicMeters` | object |  |
| `customer` | object |  |
| `customerFeedback` | object |  |
| `date` | string |  |
| `deliverToCollectFrom` | string |  |
| `department` | object |  |
| `depot` | object |  |
| `depotAddress` | object |  |
| `depotContact` | object |  |
| `depotContactNo` | object |  |
| `destinationTimeWindow` | object |  |
| `detrackNumber` | string |  |
| `doNumber` | string |  |
| `door` | object |  |
| `driverMobileNumber` | object |  |
| `driverRating` | object |  |
| `envelopes` | object |  |
| `etaTime` | object |  |
| `faxNumber` | object |  |
| `geofenceAckAt` | object |  |
| `geofenceAckLat` | object |  |
| `geofenceAckLng` | object |  |
| `goodsServiceRating` | object |  |
| `groupCode` | object |  |
| `groupId` | object |  |
| `groupName` | object |  |
| `headToDeliveryAt` | object |  |
| `holdTime` | object |  |
| `id` | string |  |
| `identificationNumber` | object |  |
| `instructions` | object |  |
| `insuranceCoverage` | boolean |  |
| `insurancePrice` | object |  |
| `invoiceAmount` | object |  |
| `invoiceNumber` | object |  |
| `items[].actualQuantity` | object |  |
| `items[].batchNumber` | object |  |
| `items[].checked` | boolean |  |
| `items[].comments` | object |  |
| `items[].description` | object |  |
| `items[].expiryDate` | object |  |
| `items[].fixedPrice` | object |  |
| `items[].followUpQuantity` | object |  |
| `items[].followUpReason` | object |  |
| `items[].id` | string |  |
| `items[].inboundQuantity` | object |  |
| `items[].minimumQuantity` | object |  |
| `items[].photoUrl` | object |  |
| `items[].purchaseOrderNumber` | object |  |
| `items[].quantity` | object |  |
| `items[].rejectQuantity` | number |  |
| `items[].rejectReason` | object |  |
| `items[].reworkQuantity` | object |  |
| `items[].reworkReason` | object |  |
| `items[].serialNumbers` | string |  |
| `items[].sku` | object |  |
| `items[].unitOfMeasure` | object |  |
| `items[].unitPrice` | object |  |
| `items[].unloadTimeActual` | object |  |
| `items[].unloadTimeEstimate` | object |  |
| `items[].weight` | object |  |
| `itemsCount` | number |  |
| `jobAge` | number |  |
| `jobFee` | object |  |
| `jobOrder` | object |  |
| `jobOwner` | object |  |
| `jobPrice` | object |  |
| `jobReceivedDate` | object |  |
| `jobReleaseTime` | object |  |
| `jobSequence` | object |  |
| `jobTime` | object |  |
| `jobType` | object |  |
| `lastName` | object |  |
| `liveEta` | object |  |
| `lockerAddress` | object |  |
| `lockerError` | object |  |
| `lockerLat` | object |  |
| `lockerLng` | object |  |
| `lockerStationId` | object |  |
| `lockerTransactionId` | object |  |
| `lockerTransactionStatus` | object |  |
| `marketplaceOffer` | object |  |
| `massPod` | object |  |
| `milestones[].assignTo` | string |  |
| `milestones[].createdAt` | string |  |
| `milestones[].podAt` | string |  |
| `milestones[].reason` | object |  |
| `milestones[].status` | string |  |
| `milestones[].userName` | string |  |
| `note` | object |  |
| `notifyEmail` | object |  |
| `numberOfShippingLabels` | object |  |
| `onDemand` | boolean |  |
| `openToMarketplace` | object |  |
| `orderNumber` | object |  |
| `otherPhoneNumbers` | object |  |
| `pallets` | object |  |
| `parcelHeight` | object |  |
| `parcelLength` | object |  |
| `parcelWidth` | object |  |
| `payerType` | object |  |
| `paymentAmount` | object |  |
| `paymentCollected` | object |  |
| `paymentMode` | object |  |
| `phoneNumber` | object |  |
| `photo10At` | object |  |
| `photo10FileUrl` | object |  |
| `photo1At` | object |  |
| `photo1FileUrl` | object |  |
| `photo2At` | object |  |
| `photo2FileUrl` | object |  |
| `photo3At` | object |  |
| `photo3FileUrl` | object |  |
| `photo4At` | object |  |
| `photo4FileUrl` | object |  |
| `photo5At` | object |  |
| `photo5FileUrl` | object |  |
| `photo6At` | object |  |
| `photo6FileUrl` | object |  |
| `photo7At` | object |  |
| `photo7FileUrl` | object |  |
| `photo8At` | object |  |
| `photo8FileUrl` | object |  |
| `photo9At` | object |  |
| `photo9FileUrl` | object |  |
| `photoPreviewAckAt` | object |  |
| `photoPreviewAckLat` | object |  |
| `photoPreviewAckLng` | object |  |
| `pickUpPhotoPreviewAckAt` | object |  |
| `pickUpPhotoPreviewAckLat` | object |  |
| `pickUpPhotoPreviewAckLng` | object |  |
| `pieces` | object |  |
| `podAddress` | string |  |
| `podAt` | object |  |
| `podGpsPermission` | object |  |
| `podGpsStatus` | object |  |
| `podLat` | string |  |
| `podLng` | string |  |
| `podTime` | object |  |
| `postalCode` | object |  |
| `primaryJobStatus` | string |  |
| `priority` | object |  |
| `rateCardChargeable` | object |  |
| `rateCardChargeableId` | object |  |
| `rateCardId` | object |  |
| `rateCardVersion` | object |  |
| `reason` | object |  |
| `reattempted` | object |  |
| `receivedBySentBy` | object |  |
| `recipientSenderDevicePodAt` | object |  |
| `recipientSenderDeviceSignatureFileUrl` | object |  |
| `recipientSenderDeviceSignedBy` | object |  |
| `remarks` | object |  |
| `rolls` | object |  |
| `runNumber` | object |  |
| `salesPerson` | object |  |
| `senderPhoneNumber` | object |  |
| `serialNumber` | object |  |
| `serviceTime` | object |  |
| `serviceType` | object |  |
| `signatureFileUrl` | object |  |
| `signedAt` | object |  |
| `source` | object |  |
| `startDate` | string |  |
| `state` | object |  |
| `status` | string |  |
| `temperature` | object |  |
| `textedAt` | object |  |
| `timeWindow` | object |  |
| `timeWindowFrom` | object |  |
| `timeWindowTo` | object |  |
| `timeZone` | object |  |
| `totalPrice` | object |  |
| `trackingLink` | string |  |
| `trackingNumber` | object |  |
| `trackingStatus` | string |  |
| `trackingStatusCode` | string |  |
| `trays` | object |  |
| `type` | string |  |
| `updatedAt` | string |  |
| `useLocker` | boolean |  |
| `vehicleType` | object |  |
| `verificationCode` | number |  |
| `warehouseAddress` | object |  |
| `webhookUrl` | object |  |
| `weight` | object |  |
| `zone` | object |  |

## Native endpoint

Through the native Detrack API, this operation is `POST /dn/jobs/reattempt` (base URL `https://app.detrack.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/reattempt-job.md) for the provider-specific parameters and requirements.

