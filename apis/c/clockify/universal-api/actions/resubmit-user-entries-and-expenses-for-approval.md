# Clockify: Resubmit User Entries and Expenses for Approval

Resubmits a user's entries and expenses for approval in Clockify.

```
POST https://connect.mindcloud.co/v1/universal/clockify/latest/actions/resubmit-user-entries-and-expenses-for-approval
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clockify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/clockify/latest/actions/resubmit-user-entries-and-expenses-for-approval" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workspaceId": "string",
  "userId": "string",
  "periodStart": "2026-01-01"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clockify/latest/actions/resubmit-user-entries-and-expenses-for-approval', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workspaceId": "string",
    "userId": "string",
    "periodStart": "2026-01-01"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workspaceId` | list<string> | yes |  |
| `userId` | string<string> | yes |  |
| `periodStart` | string | yes | Example: `2026-01-01`. |
| `period` | list<string> | no | One of: `MONTHLY`, `SEMI_MONTHLY`, `WEEKLY`. |

## Response

```json
{
  "success": true,
  "data": [
    {
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
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `creator` | object |  |
| `creator.userEmail` | string |  |
| `creator.userId` | string |  |
| `creator.userName` | string |  |
| `dateRange` | object |  |
| `dateRange.end` | date |  |
| `dateRange.start` | date |  |
| `id` | string |  |
| `owner` | object |  |
| `owner.startOfWeek` | string |  |
| `owner.timeZone` | string |  |
| `owner.userId` | string |  |
| `owner.userName` | string |  |
| `status` | object |  |
| `status.note` | string |  |
| `status.state` | string |  |
| `status.updatedAt` | date |  |
| `status.updatedBy` | string |  |
| `status.updatedByUserName` | string |  |
| `workspaceId` | string |  |

## Native endpoint

Through the native Clockify API, this operation is `POST workspaces/:workspaceId/approval-requests/users/:userId/resubmit-entries-for-approval` (base URL `https://api.clockify.me/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/resubmit-user-entries-and-expenses-for-approval.md) for the provider-specific parameters and requirements.

