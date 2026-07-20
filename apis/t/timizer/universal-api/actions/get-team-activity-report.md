# Timizer: Get Team Activity Report

Retrieves a team activity report from Timizer.

```
GET https://connect.mindcloud.co/v1/universal/timizer/latest/actions/get-team-activity-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timizer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timizer/latest/actions/get-team-activity-report?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timizer/latest/actions/get-team-activity-report?${params}`, {
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
| `activityReportId` | string | no | ID of the activity report. |
| `teamId` | string | no | ID of the team. |

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

Through the native Timizer API, this operation is `GET /app/admin-teams/:teamId/activity-reports/:activityReportId` (base URL `https://api.timizer.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-team-activity-report.md) for the provider-specific parameters and requirements.

