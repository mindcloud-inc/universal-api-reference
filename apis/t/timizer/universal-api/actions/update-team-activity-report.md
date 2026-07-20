# Timizer: Update Team Activity Report

Updates an existing team activity report in Timizer.

```
PUT https://connect.mindcloud.co/v1/universal/timizer/latest/actions/update-team-activity-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timizer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/timizer/latest/actions/update-team-activity-report" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "teamId": 1,
  "activityReportId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/timizer/latest/actions/update-team-activity-report', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "teamId": 1,
    "activityReportId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `teamId` | number | yes | ID of the team. |
| `activityReportId` | number | yes | ID of the activity report. |
| `clientId` | number | no | ID of the client. |
| `contractedId` | number | no | ID of the contracted company. |
| `year` | number | no | Target year. |
| `month` | number | no | Target month. |
| `type` | list | no | Activity report type. One of: `day`, `hour`. |
| `missionId` | number | no | Optional mission ID. |
| `clientContactId` | number | no | Optional client contact ID. |
| `contractedContactId` | number | no | Optional contracted contact ID. |
| `rating` | number | no | Optional rating. |
| `note` | string | no | Optional activity report note. |
| `workDays[]` | array<object> | no | Work day entries for the activity report. |
| `workDays[].dayOfMonth` | number | no | Day of month for the work entry. |
| `workDays[].workedTime` | list | no | Worked time enum for the work entry. One of: `custom`, `full`, `half`, `none`. |
| `workDays[].workedSeconds` | number | no | Worked seconds for custom time entries. |
| `workDays[].note` | string | no | Optional note for the work entry. |
| `workDays[].tags[]` | array<object> | no | Optional tags for the work entry. |
| `workDays[].tags[].id` | number | no | Optional tag ID. |
| `workDays[].tags[].label` | string | no | Tag label. |
| `workDays[].tags[].customId` | string | no | Optional tag custom ID. |
| `workDays[].tags[].textColor` | string | no | Optional tag text color. |
| `workDays[].tags[].backgroundColor` | string | no | Optional tag background color. |
| `workDays[].tags[].weight` | number | no | Optional tag weight. |
| `workDays[].tags[].workable` | boolean | no | Whether the tag is workable. |
| `workDays[].tags[].pricePerUnit` | number | no | Optional tag price per unit. |
| `workDays[].tags[].costPerUnit` | number | no | Optional tag cost per unit. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "client": {},
      "clientContact": {},
      "comment": "string",
      "contracted": {},
      "contractedContact": {},
      "createdAt": "2026-05-07T12:00:00.000Z",
      "hasAvailableTags": true,
      "hasDocuments": true,
      "hasExpenseReports": true,
      "hasInvoices": true,
      "id": 1,
      "isProcessed": true,
      "mission": {},
      "month": 1,
      "note": "string",
      "pennylaneInvoiceId": 1,
      "qontoInvoiceId": 1,
      "rating": 1,
      "shareable": true,
      "teamId": 1,
      "tiimeInvoiceId": 1,
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "user": {},
      "workDays": [
        {}
      ],
      "workflowStepName": "Ava Chen",
      "year": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `client` | object |  |
| `clientContact` | object |  |
| `comment` | string |  |
| `contracted` | object |  |
| `contractedContact` | object |  |
| `createdAt` | date |  |
| `hasAvailableTags` | boolean |  |
| `hasDocuments` | boolean |  |
| `hasExpenseReports` | boolean |  |
| `hasInvoices` | boolean |  |
| `id` | number |  |
| `isProcessed` | boolean |  |
| `mission` | object |  |
| `month` | number |  |
| `note` | string |  |
| `pennylaneInvoiceId` | number |  |
| `qontoInvoiceId` | number |  |
| `rating` | number |  |
| `shareable` | boolean |  |
| `teamId` | number |  |
| `tiimeInvoiceId` | number |  |
| `type` | string |  |
| `updatedAt` | date |  |
| `user` | object |  |
| `workDays` | array<object> |  |
| `workflowStepName` | string |  |
| `year` | number |  |

## Native endpoint

Through the native Timizer API, this operation is `PATCH /app/admin-teams/:teamId/activity-reports/:activityReportId` (base URL `https://api.timizer.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-team-activity-report.md) for the provider-specific parameters and requirements.

