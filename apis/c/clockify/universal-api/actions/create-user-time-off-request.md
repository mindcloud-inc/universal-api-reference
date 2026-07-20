# Clockify: Create User Time Off Request

Creates a time off request for a user in Clockify.

```
POST https://connect.mindcloud.co/v1/universal/clockify/latest/actions/create-user-time-off-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clockify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/clockify/latest/actions/create-user-time-off-request" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workspaceId": "string",
  "policyId": "string",
  "userId": "string",
  "timeOffPeriod": {},
  "timeOffPeriod.period": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clockify/latest/actions/create-user-time-off-request', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workspaceId": "string",
    "policyId": "string",
    "userId": "string",
    "timeOffPeriod": {},
    "timeOffPeriod.period": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workspaceId` | list<string> | yes |  |
| `policyId` | string<string> | yes |  |
| `userId` | string<string> | yes |  |
| `timeOffPeriod` | object | yes |  |
| `note` | string | no | Example: `Sample note`. |
| `timeOffPeriod.halfDayPeriod` | string | no |  |
| `timeOffPeriod.isHalfDay` | boolean | no |  |
| `timeOffPeriod.period` | object | yes |  |
| `timeOffPeriod.period.days` | number | no |  |
| `timeOffPeriod.period.end` | string | no |  |
| `timeOffPeriod.period.start` | string | no |  |
| `timeOffPeriod.timeOffHalfDayPeriod` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "balance": 1,
      "balanceDiff": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "note": "string",
      "policyId": "string",
      "policyName": "Ava Chen",
      "requesterUserId": "string",
      "requesterUserName": "Ava Chen",
      "status": {
        "changedAt": "2026-05-07T12:00:00.000Z",
        "changedByUserId": "string",
        "changedByUserName": "Ava Chen",
        "changedForUserName": "Ava Chen",
        "note": "string",
        "statusType": "string"
      },
      "timeOffPeriod": {
        "halfDay": true,
        "halfDayHours": {
          "end": "2026-05-07T12:00:00.000Z",
          "start": "2026-05-07T12:00:00.000Z"
        },
        "halfDayPeriod": "string",
        "period": {
          "end": "2026-05-07T12:00:00.000Z",
          "start": "2026-05-07T12:00:00.000Z"
        }
      },
      "timeUnit": "string",
      "userEmail": "ava@example.com",
      "userId": "string",
      "userName": "Ava Chen",
      "userTimeZone": "string",
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `balance` | number |  |
| `balanceDiff` | number |  |
| `createdAt` | date |  |
| `id` | string |  |
| `note` | string |  |
| `policyId` | string |  |
| `policyName` | string |  |
| `requesterUserId` | string |  |
| `requesterUserName` | string |  |
| `status` | object |  |
| `status.changedAt` | date |  |
| `status.changedByUserId` | string |  |
| `status.changedByUserName` | string |  |
| `status.changedForUserName` | string |  |
| `status.note` | string |  |
| `status.statusType` | string |  |
| `timeOffPeriod` | object |  |
| `timeOffPeriod.halfDay` | boolean |  |
| `timeOffPeriod.halfDayHours` | object |  |
| `timeOffPeriod.halfDayHours.end` | date |  |
| `timeOffPeriod.halfDayHours.start` | date |  |
| `timeOffPeriod.halfDayPeriod` | string |  |
| `timeOffPeriod.period` | object |  |
| `timeOffPeriod.period.end` | date |  |
| `timeOffPeriod.period.start` | date |  |
| `timeUnit` | string |  |
| `userEmail` | string |  |
| `userId` | string |  |
| `userName` | string |  |
| `userTimeZone` | string |  |
| `workspaceId` | string |  |

## Native endpoint

Through the native Clockify API, this operation is `POST workspaces/:workspaceId/time-off/policies/:policyId/users/:userId/requests` (base URL `https://api.clockify.me/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-user-time-off-request.md) for the provider-specific parameters and requirements.

