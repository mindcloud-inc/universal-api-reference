# CoachAccountable: List Engagements

Retrieves engagements from CoachAccountable.

```
GET https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/list-engagements
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CoachAccountable `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/list-engagements?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/list-engagements?${params}`, {
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
| `clientId` | number | no | Filter Engagements by Client. |
| `companyId` | number | no | Filter Engagements by Company. |
| `startDateFrom` | date | no | Set to restrict Engagements returned to those with a start date at or after the provided value. |
| `startDateTo` | date | no | Set to restrict Engagements returned to those with a start date at or before the provided value. |
| `endDateFrom` | date | no | Set to restrict Engagements returned to those with an end date at or after the provided value. |
| `endDateTo` | date | no | Set to restrict Engagements returned to those with an end date at or before the provided value. |
| `includeAppointments` | boolean | no | Set to true to include Appointments which count towards the Engagement. Default: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "allocation": 1,
      "allocationPerClient": 1,
      "allocationUnits": "string",
      "allocationUsedA": 1,
      "allocationUsedP": 1,
      "allocationUsedV": 1,
      "AppointmentSet": [
        {
          "ClientID": 1,
          "CoachID": 1,
          "countsInEngagement": 1,
          "dateAdded": "2026-05-07T12:00:00.000Z",
          "dateCanceled": "2026-05-07T12:00:00.000Z",
          "endDate": "2026-05-07T12:00:00.000Z",
          "ID": 1,
          "startDate": "2026-05-07T12:00:00.000Z",
          "status": "string",
          "what": "string"
        }
      ],
      "ClientID": 1,
      "CoachID": 1,
      "CompanyID": 1,
      "dateAdded": "2026-05-07T12:00:00.000Z",
      "dateClosed": "2026-05-07T12:00:00.000Z",
      "endDate": "2026-05-07T12:00:00.000Z",
      "ID": 1,
      "isCanceled": true,
      "isComplete": true,
      "name": "Ava Chen",
      "nextInvoiceDate": "2026-05-07T12:00:00.000Z",
      "startDate": "2026-05-07T12:00:00.000Z",
      "type": "string",
      "withName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allocation` | number |  |
| `allocationPerClient` | number |  |
| `allocationUnits` | string |  |
| `allocationUsedA` | number |  |
| `allocationUsedP` | number |  |
| `allocationUsedV` | number |  |
| `AppointmentSet` | array<object> |  |
| `AppointmentSet[].ClientID` | number |  |
| `AppointmentSet[].CoachID` | number |  |
| `AppointmentSet[].countsInEngagement` | number |  |
| `AppointmentSet[].dateAdded` | date |  |
| `AppointmentSet[].dateCanceled` | date |  |
| `AppointmentSet[].endDate` | date |  |
| `AppointmentSet[].ID` | number |  |
| `AppointmentSet[].startDate` | date |  |
| `AppointmentSet[].status` | string |  |
| `AppointmentSet[].what` | string |  |
| `ClientID` | number |  |
| `CoachID` | number |  |
| `CompanyID` | number |  |
| `dateAdded` | date |  |
| `dateClosed` | date |  |
| `endDate` | date |  |
| `ID` | number |  |
| `isCanceled` | boolean |  |
| `isComplete` | boolean |  |
| `name` | string |  |
| `nextInvoiceDate` | date |  |
| `startDate` | date |  |
| `type` | string |  |
| `withName` | string |  |

## Native endpoint

Through the native CoachAccountable API, this operation is `POST /` (base URL `https://www.coachaccountable.com/API`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-engagements.md) for the provider-specific parameters and requirements.

