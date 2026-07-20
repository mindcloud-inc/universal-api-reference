# Clockify: Update Approval Request

Updates an approval request in Clockify.

```
PUT https://connect.mindcloud.co/v1/universal/clockify/latest/actions/update-approval-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clockify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/clockify/latest/actions/update-approval-request" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workspaceId": "string",
  "approvalRequestId": "string",
  "state": "APPROVED"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clockify/latest/actions/update-approval-request', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workspaceId": "string",
    "approvalRequestId": "string",
    "state": "APPROVED"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workspaceId` | list<string> | yes |  |
| `approvalRequestId` | string<string> | yes |  |
| `state` | list<string> | yes | One of: `APPROVED`, `PENDING`, `REJECTED`, `WITHDRAWN_APPROVAL`, `WITHDRAWN_SUBMISSION`. |
| `note` | string | no | Example: `Sample note`. |

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

Through the native Clockify API, this operation is `PATCH workspaces/:workspaceId/approval-requests/:approvalRequestId` (base URL `https://api.clockify.me/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-approval-request.md) for the provider-specific parameters and requirements.

