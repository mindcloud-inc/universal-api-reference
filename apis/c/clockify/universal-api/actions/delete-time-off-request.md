# Clockify: Delete Time Off Request

Deletes a time off request from Clockify.

```
DELETE https://connect.mindcloud.co/v1/universal/clockify/latest/actions/delete-time-off-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clockify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/clockify/latest/actions/delete-time-off-request?connectionId=$CONNECTION_ID&workspaceId=string&policyId=string&requestId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceId": "string",
  "policyId": "string",
  "requestId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clockify/latest/actions/delete-time-off-request?${params}`, {
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
| `workspaceId` | list<string> | yes |  |
| `policyId` | string<string> | yes |  |
| `requestId` | string<string> | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "balanceDiff": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "note": "string",
      "policyId": "string",
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
      "userId": "string",
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `balanceDiff` | number |  |
| `createdAt` | date |  |
| `id` | string |  |
| `note` | string |  |
| `policyId` | string |  |
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
| `userId` | string |  |
| `workspaceId` | string |  |

## Native endpoint

Through the native Clockify API, this operation is `DELETE workspaces/:workspaceId/time-off/policies/:policyId/requests/:requestId` (base URL `https://api.clockify.me/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-time-off-request.md) for the provider-specific parameters and requirements.

