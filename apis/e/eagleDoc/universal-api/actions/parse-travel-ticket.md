# Eagle Doc: Parse Travel Ticket

Creates a travel ticket extraction in Eagle Doc.

```
POST https://connect.mindcloud.co/v1/universal/eagleDoc/latest/actions/parse-travel-ticket
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Eagle Doc `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/eagleDoc/latest/actions/parse-travel-ticket" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eagleDoc/latest/actions/parse-travel-ticket', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "file": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `file` | file | yes | Travel ticket file to upload |

## Response

```json
{
  "success": true,
  "data": [
    {
      "docType": "string",
      "general": {
        "arrivalTime": "string",
        "baggageAllowance": "string",
        "baggageFee": "string",
        "baggageWeight": "string",
        "bookingAgent": "string",
        "bookingCode": "string",
        "bookingDate": "2026-05-07T12:00:00.000Z",
        "bookingReference": "string",
        "bookingStatus": "string",
        "bookingTime": "string",
        "currency": "string",
        "departureTime": "string",
        "from": "string",
        "fullName": "Ava Chen",
        "insurancePolicyNumber": "string",
        "insuranceProvider": "string",
        "mealPreference": "string",
        "paymentMethod": "string",
        "paymentStatus": "string",
        "price": "string",
        "seatNumber": "string",
        "seatPreference": "string",
        "specialRequest": "string",
        "taxAmount": "string",
        "ticketNumber": "string",
        "to": "string",
        "totalAmount": "string",
        "travelDate": "2026-05-07T12:00:00.000Z",
        "travelInsurance": "string",
        "travelVehicle": "string"
      },
      "processingInfo": {
        "docConfigId": {},
        "docType": "string",
        "duration": "string",
        "fileHash": "string",
        "language": "string",
        "numberOfPages": "string",
        "version": "string"
      },
      "signatures": {},
      "verification": {
        "nonDuplication": {
          "flagValid": true,
          "message": "string"
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `docType` | string |  |
| `general.arrivalTime` | string |  |
| `general.baggageAllowance` | string |  |
| `general.baggageFee` | string |  |
| `general.baggageWeight` | string |  |
| `general.bookingAgent` | string |  |
| `general.bookingCode` | string |  |
| `general.bookingDate` | date |  |
| `general.bookingReference` | string |  |
| `general.bookingStatus` | string |  |
| `general.bookingTime` | string |  |
| `general.currency` | string |  |
| `general.departureTime` | string |  |
| `general.from` | string |  |
| `general.fullName` | string |  |
| `general.insurancePolicyNumber` | string |  |
| `general.insuranceProvider` | string |  |
| `general.mealPreference` | string |  |
| `general.paymentMethod` | string |  |
| `general.paymentStatus` | string |  |
| `general.price` | string |  |
| `general.seatNumber` | string |  |
| `general.seatPreference` | string |  |
| `general.specialRequest` | string |  |
| `general.taxAmount` | string |  |
| `general.ticketNumber` | string |  |
| `general.to` | string |  |
| `general.totalAmount` | string |  |
| `general.travelDate` | date |  |
| `general.travelInsurance` | string |  |
| `general.travelVehicle` | string |  |
| `processingInfo.docConfigId` | object |  |
| `processingInfo.docType` | string |  |
| `processingInfo.duration` | string |  |
| `processingInfo.fileHash` | string |  |
| `processingInfo.language` | string |  |
| `processingInfo.numberOfPages` | string |  |
| `processingInfo.version` | string |  |
| `signatures` | object |  |
| `verification.nonDuplication.flagValid` | boolean |  |
| `verification.nonDuplication.message` | string |  |

## Native endpoint

Through the native Eagle Doc API, this operation is `POST /api/anydoc/v1/processing` (base URL `https://de.eagle-doc.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/parse-travel-ticket.md) for the provider-specific parameters and requirements.

