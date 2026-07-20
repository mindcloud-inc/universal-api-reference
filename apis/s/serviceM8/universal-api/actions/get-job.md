# ServiceM8: Get Job



```
GET https://connect.mindcloud.co/v1/universal/serviceM8/latest/actions/get-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ServiceM8 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/serviceM8/latest/actions/get-job?connectionId=$CONNECTION_ID&uuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "uuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/serviceM8/latest/actions/get-job?${params}`, {
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
| `uuid` | string | yes | Record UUID of the job to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": 1,
      "badges": "string",
      "billingAddress": "string",
      "categoryUuid": "string",
      "companyUuid": "string",
      "completionActionedByUuid": "string",
      "completionDate": "2026-05-07T12:00:00.000Z",
      "createdByStaffUuid": "string",
      "date": "2026-05-07T12:00:00.000Z",
      "editDate": "2026-05-07T12:00:00.000Z",
      "generatedJobId": "string",
      "geoCity": "string",
      "geoCountry": "string",
      "geoIsValid": 1,
      "geoNumber": "string",
      "geoPostcode": "string",
      "geoState": "string",
      "geoStreet": "string",
      "invoiceSent": true,
      "invoiceSentStamp": "2026-05-07T12:00:00.000Z",
      "jobAddress": "string",
      "jobDescription": "string",
      "jobIsScheduledUntilStamp": "2026-05-07T12:00:00.000Z",
      "lat": 1,
      "lng": 1,
      "paymentActionedByUuid": "string",
      "paymentAmount": 1,
      "paymentDate": "2026-05-07T12:00:00.000Z",
      "paymentMethod": "string",
      "paymentNote": "string",
      "paymentProcessed": 1,
      "paymentProcessedStamp": "2026-05-07T12:00:00.000Z",
      "paymentReceived": 1,
      "paymentReceivedStamp": "2026-05-07T12:00:00.000Z",
      "purchaseOrderNumber": "string",
      "queueAssignedStaffUuid": "string",
      "queueExpiryDate": "2026-05-07T12:00:00.000Z",
      "queueUuid": "string",
      "quoteDate": "2026-05-07T12:00:00.000Z",
      "quoteSent": true,
      "quoteSentStamp": "2026-05-07T12:00:00.000Z",
      "readyToInvoice": "string",
      "readyToInvoiceStamp": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "totalInvoiceAmount": "string",
      "unsuccessfulDate": "2026-05-07T12:00:00.000Z",
      "uuid": "string",
      "workDoneDescription": "string",
      "workOrderDate": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | number |  |
| `badges` | string |  |
| `billingAddress` | string |  |
| `categoryUuid` | string |  |
| `companyUuid` | string |  |
| `completionActionedByUuid` | string |  |
| `completionDate` | date |  |
| `createdByStaffUuid` | string |  |
| `date` | date |  |
| `editDate` | date |  |
| `generatedJobId` | string |  |
| `geoCity` | string |  |
| `geoCountry` | string |  |
| `geoIsValid` | number |  |
| `geoNumber` | string |  |
| `geoPostcode` | string |  |
| `geoState` | string |  |
| `geoStreet` | string |  |
| `invoiceSent` | boolean |  |
| `invoiceSentStamp` | date |  |
| `jobAddress` | string |  |
| `jobDescription` | string |  |
| `jobIsScheduledUntilStamp` | date |  |
| `lat` | number |  |
| `lng` | number |  |
| `paymentActionedByUuid` | string |  |
| `paymentAmount` | number |  |
| `paymentDate` | date |  |
| `paymentMethod` | string |  |
| `paymentNote` | string |  |
| `paymentProcessed` | number |  |
| `paymentProcessedStamp` | date |  |
| `paymentReceived` | number |  |
| `paymentReceivedStamp` | date |  |
| `purchaseOrderNumber` | string |  |
| `queueAssignedStaffUuid` | string |  |
| `queueExpiryDate` | date |  |
| `queueUuid` | string |  |
| `quoteDate` | date |  |
| `quoteSent` | boolean |  |
| `quoteSentStamp` | date |  |
| `readyToInvoice` | string |  |
| `readyToInvoiceStamp` | date |  |
| `status` | string |  |
| `totalInvoiceAmount` | string |  |
| `unsuccessfulDate` | date |  |
| `uuid` | string |  |
| `workDoneDescription` | string |  |
| `workOrderDate` | date |  |

## Native endpoint

Through the native ServiceM8 API, this operation is `GET /api_1.0/job/:uuid.json` (base URL `https://api.servicem8.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-job.md) for the provider-specific parameters and requirements.

