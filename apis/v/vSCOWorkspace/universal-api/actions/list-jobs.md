# VSCO Workspace: List Jobs

Retrieves jobs from VSCO Workspace.

```
GET https://connect.mindcloud.co/v1/universal/vSCOWorkspace/latest/actions/list-jobs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a VSCO Workspace `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vSCOWorkspace/latest/actions/list-jobs?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vSCOWorkspace/latest/actions/list-jobs?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "accountBalance": {},
      "bookingDate": "2026-05-07T12:00:00.000Z",
      "brandId": "string",
      "closed": true,
      "closedDate": "2026-05-07T12:00:00.000Z",
      "closedReasonId": "string",
      "closedReasonName": "Ava Chen",
      "completedDate": "2026-05-07T12:00:00.000Z",
      "contactFormId": "string",
      "created": "2026-05-07T12:00:00.000Z",
      "creditBalance": {},
      "customFields": [
        {}
      ],
      "customNumber": "string",
      "eventDate": "2026-05-07T12:00:00.000Z",
      "externalMappings": [
        {}
      ],
      "fulfillmentDate": "2026-05-07T12:00:00.000Z",
      "guestCount": 1,
      "id": "string",
      "inquiryDate": "2026-05-07T12:00:00.000Z",
      "jobTypeId": "string",
      "jobTypeName": "Ava Chen",
      "lastClientActivity": {},
      "leadConfidence": "string",
      "leadDecisionExpectedByDate": "2026-05-07T12:00:00.000Z",
      "leadMaxBudget": 1,
      "leadNotes": "string",
      "leadRating": 1,
      "leadSourceId": "string",
      "leadSourceName": "Ava Chen",
      "leadStatusChangedAt": {},
      "leadStatusId": "string",
      "leadStatusName": "Ava Chen",
      "modified": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "nextInteractionDate": {},
      "nextInteractionItem": "string",
      "pinned": true,
      "previousInteractionDate": {},
      "previousInteractionItem": "string",
      "primarySessionId": {},
      "sample": true,
      "stage": "string",
      "staleDate": {},
      "title": "string",
      "totalCost": {},
      "totalProfit": {},
      "totalRevenue": {},
      "webLead": true,
      "workflowId": "string",
      "workflowName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountBalance` | object |  |
| `bookingDate` | date | A date string consisting of year, month and day in the timezone of the event if specified or the studio. |
| `brandId` | string | A ULID entity identifier that is nullable. |
| `closed` | boolean | Whether or not the lead or job is closed. A closed reason might be provided as well. |
| `closedDate` | date | A date string consisting of year, month and day in the timezone of the event if specified or the studio. |
| `closedReasonId` | string | A ULID entity identifier that is nullable. |
| `closedReasonName` | string |  |
| `completedDate` | date | A date string consisting of year, month and day in the timezone of the event if specified or the studio. |
| `contactFormId` | string | A ULID entity identifier that is nullable. |
| `created` | date | A server timestamp (always in UTC) |
| `creditBalance` | object |  |
| `customFields` | array<object> |  |
| `customNumber` | string |  |
| `eventDate` | date | A date string consisting of year, month and day in the timezone of the event if specified or the studio. |
| `externalMappings` | array<object> |  |
| `fulfillmentDate` | date | A date string consisting of year, month and day in the timezone of the event if specified or the studio. |
| `guestCount` | number |  |
| `id` | string | A lowercase [ULID](https://github.com/ulid/spec) entity identifier |
| `inquiryDate` | date | A date string consisting of year, month and day in the timezone of the event if specified or the studio. |
| `jobTypeId` | string | A ULID entity identifier that is nullable. |
| `jobTypeName` | string |  |
| `lastClientActivity` | object |  |
| `leadConfidence` | string |  |
| `leadDecisionExpectedByDate` | date | A date string consisting of year, month and day in the timezone of the event if specified or the studio. |
| `leadMaxBudget` | number |  |
| `leadNotes` | string |  |
| `leadRating` | number |  |
| `leadSourceId` | string | A ULID entity identifier that is nullable. |
| `leadSourceName` | string |  |
| `leadStatusChangedAt` | object |  |
| `leadStatusId` | string | A ULID entity identifier that is nullable. |
| `leadStatusName` | string |  |
| `modified` | date | A server timestamp (always in UTC) |
| `name` | string | Name of the job that will override the title. |
| `nextInteractionDate` | object |  |
| `nextInteractionItem` | string |  |
| `pinned` | boolean |  |
| `previousInteractionDate` | object |  |
| `previousInteractionItem` | string |  |
| `primarySessionId` | object |  |
| `sample` | boolean | Whether or not the lead or job is a sample job. |
| `stage` | string | Specifies the stage that the job is in. |
| `staleDate` | object |  |
| `title` | string | Generated title of the job |
| `totalCost` | object |  |
| `totalProfit` | object |  |
| `totalRevenue` | object |  |
| `webLead` | boolean | Whether or not the lead or job came from a contact form. |
| `workflowId` | string | A ULID entity identifier that is nullable. |
| `workflowName` | string |  |

## Native endpoint

Through the native VSCO Workspace API, this operation is `GET /job` (base URL `https://workspace.vsco.co/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-jobs.md) for the provider-specific parameters and requirements.

