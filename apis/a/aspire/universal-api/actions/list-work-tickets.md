# Aspire: List Work Tickets

Retrieves takeoff items from your Aspire account.

```
GET https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-work-tickets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aspire `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-work-tickets?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aspire/latest/actions/list-work-tickets?${params}`, {
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
| `filter` | string | no | Optional Aspire filter expression for narrowing work tickets. |
| `orderBy` | string | no | Optional Aspire sort expression for work ticket results. |
| `select` | string | no | Optional comma-separated list of work ticket fields to return. |
| `expand` | string | no | Optional Aspire expand expression for related work ticket data. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "annualizedOccur": 1,
      "anticStartDate": "string",
      "approvedDate": "string",
      "approvedUserID": 1,
      "approvedUserName": "Ava Chen",
      "branchID": 1,
      "branchName": "Ava Chen",
      "budgetVariance": 1,
      "completeDate": "string",
      "contractYear": 1,
      "createdByUserID": 1,
      "createdByUserName": "Ava Chen",
      "createdDateTime": "string",
      "crewLeaderContactID": 1,
      "crewLeaderName": "Ava Chen",
      "distributedHours": 1,
      "earnedRevenue": 1,
      "equipCostEst": 1,
      "equipmentCostAct": 1,
      "estRealizeRateRevenue": 1,
      "hourCostEst": 1,
      "hoursAct": 1,
      "hoursEst": 1,
      "hoursScheduled": 1,
      "hoursUnscheduled": 1,
      "invoicedAmount": {},
      "invoiceID": {},
      "invoiceNumber": {},
      "laborCostAct": 1,
      "lastModifiedByUserID": 1,
      "lastModifiedByUserName": "Ava Chen",
      "lastModifiedDateTime": "string",
      "materialCostAct": 1,
      "materialCostEst": 1,
      "notes": {},
      "occur": 1,
      "occurrences": 1,
      "onSiteHours": 1,
      "onSiteOverUnder": 1,
      "onSiteVariance": 1,
      "operationsManagerContactID": {},
      "opportunityID": 1,
      "opportunityNumber": 1,
      "opportunityServiceID": 1,
      "otherCostAct": 1,
      "otherCostEst": 1,
      "oTHoursAct": 1,
      "partialOccurrence": 1,
      "percentComplete": 1,
      "price": 1,
      "realizeRateRevenue": {},
      "revenue": 1,
      "reviewedDateTime": {},
      "reviewedUserID": {},
      "reviewedUserName": {},
      "routeSupervisorContactID": {},
      "scheduledStartDate": "string",
      "startFormDateTime": {},
      "startFormUserId": {},
      "subCostAct": 1,
      "subCostEst": 1,
      "subPartialOccurrence": 1,
      "tMCalcAmount": {},
      "tMOverrideAmount": {},
      "totalCostAct": 1,
      "visitsScheduled": {},
      "warrantyHoursAct": 1,
      "workTicketID": 1,
      "workTicketNumber": 1,
      "workTicketStatus": "string",
      "workTicketStatusID": 1,
      "workTicketStatusName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `annualizedOccur` | number |  |
| `anticStartDate` | string |  |
| `approvedDate` | string |  |
| `approvedUserID` | number |  |
| `approvedUserName` | string |  |
| `branchID` | number |  |
| `branchName` | string |  |
| `budgetVariance` | number |  |
| `completeDate` | string |  |
| `contractYear` | number |  |
| `createdByUserID` | number |  |
| `createdByUserName` | string |  |
| `createdDateTime` | string |  |
| `crewLeaderContactID` | number |  |
| `crewLeaderName` | string |  |
| `distributedHours` | number |  |
| `earnedRevenue` | number |  |
| `equipCostEst` | number |  |
| `equipmentCostAct` | number |  |
| `estRealizeRateRevenue` | number |  |
| `hourCostEst` | number |  |
| `hoursAct` | number |  |
| `hoursEst` | number |  |
| `hoursScheduled` | number |  |
| `hoursUnscheduled` | number |  |
| `invoicedAmount` | object |  |
| `invoiceID` | object |  |
| `invoiceNumber` | object |  |
| `laborCostAct` | number |  |
| `lastModifiedByUserID` | number |  |
| `lastModifiedByUserName` | string |  |
| `lastModifiedDateTime` | string |  |
| `materialCostAct` | number |  |
| `materialCostEst` | number |  |
| `notes` | object |  |
| `occur` | number |  |
| `occurrences` | number |  |
| `onSiteHours` | number |  |
| `onSiteOverUnder` | number |  |
| `onSiteVariance` | number |  |
| `operationsManagerContactID` | object |  |
| `opportunityID` | number |  |
| `opportunityNumber` | number |  |
| `opportunityServiceID` | number |  |
| `otherCostAct` | number |  |
| `otherCostEst` | number |  |
| `oTHoursAct` | number |  |
| `partialOccurrence` | number |  |
| `percentComplete` | number |  |
| `price` | number |  |
| `realizeRateRevenue` | object |  |
| `revenue` | number |  |
| `reviewedDateTime` | object |  |
| `reviewedUserID` | object |  |
| `reviewedUserName` | object |  |
| `routeSupervisorContactID` | object |  |
| `scheduledStartDate` | string |  |
| `startFormDateTime` | object |  |
| `startFormUserId` | object |  |
| `subCostAct` | number |  |
| `subCostEst` | number |  |
| `subPartialOccurrence` | number |  |
| `tMCalcAmount` | object |  |
| `tMOverrideAmount` | object |  |
| `totalCostAct` | number |  |
| `visitsScheduled` | object |  |
| `warrantyHoursAct` | number |  |
| `workTicketID` | number |  |
| `workTicketNumber` | number |  |
| `workTicketStatus` | string |  |
| `workTicketStatusID` | number |  |
| `workTicketStatusName` | string |  |

## Native endpoint

Through the native Aspire API, this operation is `GET WorkTickets` (base URL `https://{{credentials.environment}}.youraspire.com/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-work-tickets.md) for the provider-specific parameters and requirements.

