# Clockify: List Approval Requests

Lists all approval requests in Clockify.

```
GET https://connect.mindcloud.co/v1/universal/clockify/latest/actions/list-approval-requests
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clockify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clockify/latest/actions/list-approval-requests?connectionId=$CONNECTION_ID&workspaceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clockify/latest/actions/list-approval-requests?${params}`, {
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
| `workspaceId` | list<string> | yes | Workspace identifier |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `status` | list<string> | no | One of: `APPROVED`, `PENDING`, `WITHDRAWN_APPROVAL`. Example: `ACTIVE`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "approvalRequest": {
        "creator": {
          "userEmail": "ava@example.com",
          "userId": "string",
          "userName": "Ava Chen"
        },
        "dateRange": {
          "end": "2026-05-07T12:00:00.000Z",
          "start": "2026-05-07T12:00:00.000Z"
        },
        "id": "string",
        "owner": {
          "startOfWeek": "string",
          "timeZone": "string",
          "userId": "string",
          "userName": "Ava Chen"
        },
        "status": {
          "note": "string",
          "state": "string",
          "updatedAt": "2026-05-07T12:00:00.000Z",
          "updatedBy": "string",
          "updatedByUserName": "Ava Chen"
        },
        "workspaceId": "string"
      },
      "approvedTime": "string",
      "billableAmount": 1,
      "billableTime": "string",
      "breakTime": "string",
      "costAmount": 1,
      "entries": [
        [
          {}
        ]
      ],
      "expenses": [
        [
          {}
        ]
      ],
      "expenseTotal": 1,
      "pendingTime": "string",
      "trackedTime": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `approvalRequest` | object |  |
| `approvalRequest.creator` | object |  |
| `approvalRequest.creator.userEmail` | string |  |
| `approvalRequest.creator.userId` | string |  |
| `approvalRequest.creator.userName` | string |  |
| `approvalRequest.dateRange` | object |  |
| `approvalRequest.dateRange.end` | date |  |
| `approvalRequest.dateRange.start` | date |  |
| `approvalRequest.id` | string |  |
| `approvalRequest.owner` | object |  |
| `approvalRequest.owner.startOfWeek` | string |  |
| `approvalRequest.owner.timeZone` | string |  |
| `approvalRequest.owner.userId` | string |  |
| `approvalRequest.owner.userName` | string |  |
| `approvalRequest.status` | object |  |
| `approvalRequest.status.note` | string |  |
| `approvalRequest.status.state` | string |  |
| `approvalRequest.status.updatedAt` | date |  |
| `approvalRequest.status.updatedBy` | string |  |
| `approvalRequest.status.updatedByUserName` | string |  |
| `approvalRequest.workspaceId` | string |  |
| `approvedTime` | string |  |
| `billableAmount` | number |  |
| `billableTime` | string |  |
| `breakTime` | string |  |
| `costAmount` | number |  |
| `entries[]` | array<object> |  |
| `entries[].approvalRequestId` | string |  |
| `entries[].billable` | boolean |  |
| `entries[].costRate` | object |  |
| `entries[].costRate.amount` | number |  |
| `entries[].costRate.currency` | string |  |
| `entries[].customFieldValues[]` | array<object> |  |
| `entries[].customFieldValues[].customFieldId` | string |  |
| `entries[].customFieldValues[].sourceType` | string |  |
| `entries[].customFieldValues[].timeEntryId` | string |  |
| `entries[].customFieldValues[].value` | object |  |
| `entries[].description` | string |  |
| `entries[].hourlyRate` | object |  |
| `entries[].hourlyRate.amount` | number |  |
| `entries[].hourlyRate.currency` | string |  |
| `entries[].id` | string |  |
| `entries[].isLocked` | boolean |  |
| `entries[].project` | object |  |
| `entries[].project.clientId` | string |  |
| `entries[].project.clientName` | string |  |
| `entries[].project.color` | string |  |
| `entries[].project.id` | string |  |
| `entries[].project.name` | string |  |
| `entries[].tags[]` | array<object> |  |
| `entries[].tags[].archived` | boolean |  |
| `entries[].tags[].id` | string |  |
| `entries[].tags[].name` | string |  |
| `entries[].tags[].workspaceId` | string |  |
| `entries[].task` | object |  |
| `entries[].task.id` | string |  |
| `entries[].task.name` | string |  |
| `entries[].timeInterval` | object |  |
| `entries[].timeInterval.duration` | string |  |
| `entries[].timeInterval.end` | date |  |
| `entries[].timeInterval.offsetEnd` | number |  |
| `entries[].timeInterval.offsetStart` | number |  |
| `entries[].timeInterval.start` | date |  |
| `entries[].timeInterval.timeZone` | string |  |
| `entries[].timeInterval.zonedEnd` | date |  |
| `entries[].timeInterval.zonedStart` | date |  |
| `entries[].type` | string |  |
| `expenses[]` | array<object> |  |
| `expenses[].approvalRequestId` | string |  |
| `expenses[].approvalStatus` | string |  |
| `expenses[].billable` | boolean |  |
| `expenses[].category` | object |  |
| `expenses[].category.archived` | boolean |  |
| `expenses[].category.hasUnitPrice` | boolean |  |
| `expenses[].category.id` | string |  |
| `expenses[].category.name` | string |  |
| `expenses[].category.priceInCents` | number |  |
| `expenses[].category.unit` | string |  |
| `expenses[].category.workspaceId` | string |  |
| `expenses[].currency` | string |  |
| `expenses[].date` | string |  |
| `expenses[].fileId` | string |  |
| `expenses[].fileName` | string |  |
| `expenses[].fileUrl` | string |  |
| `expenses[].id` | string |  |
| `expenses[].isLocked` | boolean |  |
| `expenses[].locked` | boolean |  |
| `expenses[].notes` | string |  |
| `expenses[].project` | object |  |
| `expenses[].project.clientId` | string |  |
| `expenses[].project.clientName` | string |  |
| `expenses[].project.color` | string |  |
| `expenses[].project.id` | string |  |
| `expenses[].project.name` | string |  |
| `expenses[].quantity` | number |  |
| `expenses[].task` | object |  |
| `expenses[].task.id` | string |  |
| `expenses[].task.name` | string |  |
| `expenses[].total` | number |  |
| `expenses[].userId` | string |  |
| `expenses[].workspaceId` | string |  |
| `expenseTotal` | number |  |
| `pendingTime` | string |  |
| `trackedTime` | string |  |

## Native endpoint

Through the native Clockify API, this operation is `GET workspaces/:workspaceId/approval-requests` (base URL `https://api.clockify.me/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-approval-requests.md) for the provider-specific parameters and requirements.

