# Aspire: List Work Ticket Times

Start and end time for a crew member during a visit for a work ticket.

```
GET https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-work-ticket-times
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aspire `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-work-ticket-times?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-work-ticket-times?${params}`, {
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
| `expand` | string | no |  |
| `filter` | string | no |  |
| `orderBy` | string | no |  |
| `select` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "acceptedDateTime": {},
      "acceptedUserID": {},
      "acceptedUserName": {},
      "approvedDateTime": {},
      "approvedUserID": {},
      "approvedUserName": {},
      "baseHourlyRate": 1,
      "baseLaborBurdenCost": 1,
      "baseLaborCost": 1,
      "branchID": {},
      "branchName": {},
      "branchTimeZone": {},
      "breakTime": {},
      "burdenedCost": 1,
      "contactID": 1,
      "contactName": "Ava Chen",
      "createdByUserID": 1,
      "createdByUserName": "Ava Chen",
      "createdDateTime": "string",
      "crewLeaderContactID": 1,
      "crewLeaderContactName": "Ava Chen",
      "distributedTime": true,
      "endTime": "string",
      "exportedDateTime": {},
      "exportedUserID": {},
      "exportedUserName": {},
      "gEOLocationEndLatitude": {},
      "gEOLocationEndLongitude": {},
      "gEOLocationStartLatitude": {},
      "gEOLocationStartLongitude": {},
      "hasBreakTime": {},
      "hours": 1,
      "invoiceID": {},
      "invoiceNumber": {},
      "lastModifiedByUserID": 1,
      "lastModifiedByUserName": "Ava Chen",
      "lastModifiedDateTime": "string",
      "opportunityServiceLaborRate": {},
      "opportunityServiceLaborRateID": {},
      "opportunityServiceLaborRateName": {},
      "oTHours": {},
      "oTLaborBurdenCost": 1,
      "oTLaborCost": 1,
      "payCodeID": {},
      "payCodeName": {},
      "routeID": {},
      "routeName": {},
      "startTime": "string",
      "warrantyTime": true,
      "workTicketID": {},
      "workTicketNumber": {},
      "workTicketTimeDate": "string",
      "workTicketTimeID": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `acceptedDateTime` | object |  |
| `acceptedUserID` | object |  |
| `acceptedUserName` | object |  |
| `approvedDateTime` | object |  |
| `approvedUserID` | object |  |
| `approvedUserName` | object |  |
| `baseHourlyRate` | number |  |
| `baseLaborBurdenCost` | number |  |
| `baseLaborCost` | number |  |
| `branchID` | object |  |
| `branchName` | object |  |
| `branchTimeZone` | object |  |
| `breakTime` | object |  |
| `burdenedCost` | number |  |
| `contactID` | number |  |
| `contactName` | string |  |
| `createdByUserID` | number |  |
| `createdByUserName` | string |  |
| `createdDateTime` | string |  |
| `crewLeaderContactID` | number |  |
| `crewLeaderContactName` | string |  |
| `distributedTime` | boolean |  |
| `endTime` | string |  |
| `exportedDateTime` | object |  |
| `exportedUserID` | object |  |
| `exportedUserName` | object |  |
| `gEOLocationEndLatitude` | object |  |
| `gEOLocationEndLongitude` | object |  |
| `gEOLocationStartLatitude` | object |  |
| `gEOLocationStartLongitude` | object |  |
| `hasBreakTime` | object |  |
| `hours` | number |  |
| `invoiceID` | object |  |
| `invoiceNumber` | object |  |
| `lastModifiedByUserID` | number |  |
| `lastModifiedByUserName` | string |  |
| `lastModifiedDateTime` | string |  |
| `opportunityServiceLaborRate` | object |  |
| `opportunityServiceLaborRateID` | object |  |
| `opportunityServiceLaborRateName` | object |  |
| `oTHours` | object |  |
| `oTLaborBurdenCost` | number |  |
| `oTLaborCost` | number |  |
| `payCodeID` | object |  |
| `payCodeName` | object |  |
| `routeID` | object |  |
| `routeName` | object |  |
| `startTime` | string |  |
| `warrantyTime` | boolean |  |
| `workTicketID` | object |  |
| `workTicketNumber` | object |  |
| `workTicketTimeDate` | string |  |
| `workTicketTimeID` | number |  |

## Native endpoint

Through the native Aspire API, this operation is `GET WorkTicketTimes` (base URL `https://{{credentials.environment}}.youraspire.com/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-work-ticket-times.md) for the provider-specific parameters and requirements.

