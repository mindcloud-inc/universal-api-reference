# Detrack Universal API Examples

These examples use the MindCloud API key and Detrack connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Depots

Retrieves a list of depots from Detrack.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/detrack/latest/actions/list-depots?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/detrack/latest/actions/list-depots?${params}`, {
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
      "addr1": {},
      "addr2": {},
      "addr3": {},
      "address": "string",
      "addressLat": 1,
      "addressLng": 1,
      "city": {},
      "country": {},
      "countryId": {},
      "id": "string",
      "location": [
        1
      ],
      "name": "Ava Chen",
      "state": {},
      "zipCode": {}
    }
  ],
  "meta": {}
}
```

See the full [List Depots action reference](actions/list-depots.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/detrack/latest/actions/list-depots).

## Batch Create Jobs

Creates multiple jobs in Detrack at once.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/detrack/latest/actions/batch-create-jobs" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "data[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/detrack/latest/actions/batch-create-jobs', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "data[]": [{}]
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
      "assignTo": "string",
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

See the full [Batch Create Jobs action reference](actions/batch-create-jobs.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/detrack/latest/actions/batch-create-jobs).
