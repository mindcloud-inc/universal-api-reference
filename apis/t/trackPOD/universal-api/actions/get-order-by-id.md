# Track-POD: Get Order By Id

Retrieves an order from Track-POD by ID.

```
GET https://connect.mindcloud.co/v1/universal/trackPOD/latest/actions/get-order-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Track-POD `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/trackPOD/latest/actions/get-order-by-id?connectionId=$CONNECTION_ID&id=31cc9a7a-5658-4f7a-8c7c-99fe7f7173d6" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "31cc9a7a-5658-4f7a-8c7c-99fe7f7173d6"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/trackPOD/latest/actions/get-order-by-id?${params}`, {
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
| `id` | string | yes | Track-POD unique identifier for the order. Example: `31cc9a7a-5658-4f7a-8c7c-99fe7f7173d6`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Address": "string",
      "AddressId": "string",
      "AddressLat": 1,
      "AddressLon": 1,
      "AddressNote": "string",
      "AddressZone": "string",
      "ArrivedDate": "2026-05-07T12:00:00.000Z",
      "Barcode": "string",
      "ChangeDate": "2026-05-07T12:00:00.000Z",
      "Client": "string",
      "ClientId": "string",
      "ClientNote": "string",
      "COD": 1,
      "CODActual": "string",
      "ContactName": "Ava Chen",
      "CreateDateUtc": "2026-05-07T12:00:00.000Z",
      "CreateSource": {},
      "CustomerReferenceId": "string",
      "CustomFields": [
        {}
      ],
      "Date": "2026-05-07T12:00:00.000Z",
      "DeliveryInstructions": "string",
      "DepartedDate": "2026-05-07T12:00:00.000Z",
      "Depot": "string",
      "DepotId": "string",
      "DistanceFromDepotPlan": 1,
      "DriverComment": "string",
      "DriverLogin": "string",
      "DriverName": "Ava Chen",
      "DriverNumber": 1,
      "DriverVehicle": "string",
      "Email": "ava@example.com",
      "ETA": "2026-05-07T12:00:00.000Z",
      "Feedback": "string",
      "FeedbackRating": 1,
      "GoodsList": [
        {}
      ],
      "HasPhoto": true,
      "HasSignaturePhoto": true,
      "Id": "string",
      "InvoiceId": "string",
      "LoadDate": "2026-05-07T12:00:00.000Z",
      "LoadSignaturePhotos": [
        "string"
      ],
      "LoadStatus": "string",
      "Note": "string",
      "NotificationsPolicy": {},
      "Number": "string",
      "Pallets": 1,
      "Phone": "string",
      "Photos": [
        "string"
      ],
      "PickupOrder": {},
      "Pin": "string",
      "Priority": "string",
      "RejectReason": "string",
      "ReportUrl": "https://example.com",
      "RescheduledTimes": 1,
      "RouteDate": "2026-05-07T12:00:00.000Z",
      "RouteNumber": "string",
      "RoutePriority": 1,
      "RouteStatus": {},
      "Scanned": true,
      "ScanRejectReason": "string",
      "SeqNumber": 1,
      "SeqNumberDriver": 1,
      "ServiceTime": 1,
      "Shipper": "string",
      "ShipperId": "string",
      "SignatureName": "Ava Chen",
      "SignaturePhotos": [
        "string"
      ],
      "Status": "string",
      "StatusDate": "2026-05-07T12:00:00.000Z",
      "StatusId": 1,
      "StatusLat": 1,
      "StatusLon": 1,
      "TeamCode": "string",
      "TimeSlotFrom": "2026-05-07T12:00:00.000Z",
      "TimeSlotTo": "2026-05-07T12:00:00.000Z",
      "TrackId": "string",
      "TrackKey": "string",
      "TrackLink": "https://example.com",
      "Type": 1,
      "UpdatedETA": "2026-05-07T12:00:00.000Z",
      "Volume": 1,
      "Weight": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Address` | string | Delivery/Pickup address |
| `AddressId` | string | Unique identifier in user accounting system |
| `AddressLat` | number | Address GPS Latitude |
| `AddressLon` | number | Address GPS Longitude |
| `AddressNote` | string | Address note |
| `AddressZone` | string | Address zone |
| `ArrivedDate` | date | Date of arrival |
| `Barcode` | string | Barcode |
| `ChangeDate` | date |  |
| `Client` | string | Client/Customer name |
| `ClientId` | string | Unique identifier in user accounting system |
| `ClientNote` | string | Client note |
| `COD` | number | Amount of Cash on Delivery |
| `CODActual` | string | Collected Paid Amount from a Client |
| `ContactName` | string | Customer’s contact name |
| `CreateDateUtc` | date | Order creation date (UTC) |
| `CreateSource` | object |  |
| `CustomerReferenceId` | string | Customer reference order identifier in user accounting system |
| `CustomFields` | array<object> | List of custom fields |
| `Date` | date | Order date, yyyy-MM-dd |
| `DeliveryInstructions` | string | Delivery Instructions from live-tracking page |
| `DepartedDate` | date | Date of Departure |
| `Depot` | string | Depot address |
| `DepotId` | string | Unique identifier in user accounting system |
| `DistanceFromDepotPlan` | number | Planned distance from depot, m |
| `DriverComment` | string | Drivers comment from mobile application |
| `DriverLogin` | string | Login of Driver |
| `DriverName` | string | Name of Driver |
| `DriverNumber` | number | Driver Number |
| `DriverVehicle` | string | Vehicle license plate number |
| `Email` | string | Customer’s e-mail |
| `ETA` | date | Estimated time of arrival |
| `Feedback` | string | Feedback |
| `FeedbackRating` | number | Feedback Rating from mobile application |
| `GoodsList` | array<object> | Goods List in Order |
| `HasPhoto` | boolean | Photo attached |
| `HasSignaturePhoto` | boolean | Signature attached |
| `Id` | string | Unique identifier in user accounting system |
| `InvoiceId` | string | Invoice identifier in user accounting system |
| `LoadDate` | date | Date of Loading |
| `LoadSignaturePhotos` | array<string> | Array of links for download jpg file (each link is available for 24h from API call) |
| `LoadStatus` | string | Status code: none; loaded; not-loaded; |
| `Note` | string | Notes to order |
| `NotificationsPolicy` | object |  |
| `Number` | string | Order/Invoice/Job/Waybill number |
| `Pallets` | number | Pallets count |
| `Phone` | string | Customer’s contact phone number |
| `Photos` | array<string> | Array of links for download jpg file (each link is available for 24h from API call) |
| `PickupOrder` | object |  |
| `Pin` | string | Confirmation pin code |
| `Priority` | string | Priority values: low, normal, high |
| `RejectReason` | string | Reject reason for order |
| `ReportUrl` | string | Link to the PDF order delivery note (available within 1 hour from the API call) |
| `RescheduledTimes` | number | Order rescheduled times |
| `RouteDate` | date | Route date |
| `RouteNumber` | string | Route number |
| `RoutePriority` | number | Route priority |
| `RouteStatus` | object |  |
| `Scanned` | boolean | Order is scanned in the mobile application |
| `ScanRejectReason` | string | Reject reason for order's scanning |
| `SeqNumber` | number | Scheduled sequence in the route |
| `SeqNumberDriver` | number | Updated sequence by driver in the route |
| `ServiceTime` | number | Desired service time, min. If seconds are specified value will be decimal |
| `Shipper` | string | Shipper/Supplier name |
| `ShipperId` | string | Unique identifier in user accounting system |
| `SignatureName` | string | Name of the person who signed |
| `SignaturePhotos` | array<string> | Array of links for download jpg file (each link is available for 24h from API call) |
| `Status` | string | Status description |
| `StatusDate` | date | Status date |
| `StatusId` | number | Status code: 1 - In Progress; 2 - Not delivered/Not collected (site issues); 3 - Delivered/Collected; 4 - Partially; 5 - Not delivered/Not collected (order issues) |
| `StatusLat` | number | Status GPS Latitude |
| `StatusLon` | number | Status GPS Longitude |
| `TeamCode` | string | Team code |
| `TimeSlotFrom` | date | Desired delivery/pickup time from, yyyy-MM-ddTHH:mm:ss or HH:mm:ss |
| `TimeSlotTo` | date | Desired delivery/pickup time till, yyyy-MM-ddTHH:mm:ss or HH:mm:ss |
| `TrackId` | string | Id for tracking order |
| `TrackKey` | string | Key for tracking order |
| `TrackLink` | string | Link for tracking order |
| `Type` | number | Order type: 0 - Delivery order; 1 - Collection order |
| `UpdatedETA` | date | Updated estimated time of arrival |
| `Volume` | number | Total volume |
| `Weight` | number | Total weight |

## Native endpoint

Through the native Track-POD API, this operation is `GET /Order/Id/:id` (base URL `https://api.track-pod.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-order-by-id.md) for the provider-specific parameters and requirements.

