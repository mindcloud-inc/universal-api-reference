# Zenoti: Get Appointments Report

Returns a simpler result than List Appointments

```
GET https://connect.mindcloud.co/v1/universal/zenoti/latest/actions/list-appointments-flat-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zenoti `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zenoti/latest/actions/list-appointments-flat-file?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zenoti/latest/actions/list-appointments-flat-file?${params}`, {
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
| `appointmentSources[].source` | list | no |  |
| `appointmentStatuses[].appointmentStatus` | list | no | Default: `-1`. |
| `centerIds[].center` | list | no |  |
| `dateType` | list | no | Default: `0`. |
| `centerIds[]` | array | no |  |
| `date` | date | no | Use this when getting results for a single date |
| `startDate` | date | no |  |
| `endDate` | date | no |  |
| `appointmentStatuses[]` | array | no |  |
| `appointmentSources[]` | array | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "actualBookedTime": "string",
      "actualServiceTime": "string",
      "addOn": "string",
      "appointmentActualInvoiceDuration": 1,
      "appointmentDate": "string",
      "bookedBy": "string",
      "bookedDate": "string",
      "bookingSource": "string",
      "businessUnit": "string",
      "centerId": "string",
      "centerName": "Ava Chen",
      "email": "ava@example.com",
      "endTime": "string",
      "equipment": "string",
      "expectedBookedTime": "string",
      "expectedServiceTime": "string",
      "firstVisit": "string",
      "gender": "string",
      "guestCode": "string",
      "guestId": "string",
      "guestName": "Ava Chen",
      "guestPriceAdjusted": "string",
      "invoiceId": "string",
      "invoiceNo": "string",
      "isGuestDuration": "string",
      "modifiedBy": "string",
      "modifiedOn": "string",
      "providerId": "string",
      "providersCode": "string",
      "rebooked": "string",
      "rebookingSource": "string",
      "recoveryTime": "string",
      "requestType": "string",
      "serviceCategory": "string",
      "servicedBy": "string",
      "serviceName": "Ava Chen",
      "serviceSubcategory": "string",
      "startTime": "string",
      "status": "string",
      "surpriseVisit": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actualBookedTime` | string |  |
| `actualServiceTime` | string |  |
| `addOn` | string |  |
| `appointmentActualInvoiceDuration` | number |  |
| `appointmentDate` | string |  |
| `bookedBy` | string |  |
| `bookedDate` | string |  |
| `bookingSource` | string |  |
| `businessUnit` | string |  |
| `centerId` | string |  |
| `centerName` | string |  |
| `email` | string |  |
| `endTime` | string |  |
| `equipment` | string |  |
| `expectedBookedTime` | string |  |
| `expectedServiceTime` | string |  |
| `firstVisit` | string |  |
| `gender` | string |  |
| `guestCode` | string |  |
| `guestId` | string |  |
| `guestName` | string |  |
| `guestPriceAdjusted` | string |  |
| `invoiceId` | string |  |
| `invoiceNo` | string |  |
| `isGuestDuration` | string |  |
| `modifiedBy` | string |  |
| `modifiedOn` | string |  |
| `providerId` | string |  |
| `providersCode` | string |  |
| `rebooked` | string |  |
| `rebookingSource` | string |  |
| `recoveryTime` | string |  |
| `requestType` | string |  |
| `serviceCategory` | string |  |
| `servicedBy` | string |  |
| `serviceName` | string |  |
| `serviceSubcategory` | string |  |
| `startTime` | string |  |
| `status` | string |  |
| `surpriseVisit` | string |  |

## Native endpoint

Through the native Zenoti API, this operation is `POST reports/appointments/flat_file` (base URL `https://api.zenoti.com/v1/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-appointments-flat-file.md) for the provider-specific parameters and requirements.

