# Clockify: Get Workspace User Capacity Total

Retrieves a workspace user capacity total from Clockify.

```
GET https://connect.mindcloud.co/v1/universal/clockify/latest/actions/get-workspace-user-capacity-total
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clockify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clockify/latest/actions/get-workspace-user-capacity-total?connectionId=$CONNECTION_ID&end=string&start=string&userId=string&workspaceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "end": "string",
  "start": "string",
  "userId": "string",
  "workspaceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clockify/latest/actions/get-workspace-user-capacity-total?${params}`, {
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
| `end` | string | yes |  |
| `page` | number | no |  |
| `pageSize` | number | no |  |
| `start` | string | yes |  |
| `userId` | string | yes |  |
| `workspaceId` | list<string> | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "capacityPerDay": 1,
      "totalHoursPerDay": [
        [
          {}
        ]
      ],
      "userId": "string",
      "userImage": "string",
      "userName": "Ava Chen",
      "userStatus": "string",
      "workingDays": "string",
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `capacityPerDay` | number |  |
| `totalHoursPerDay[]` | array<object> |  |
| `totalHoursPerDay[].date` | date |  |
| `totalHoursPerDay[].totalHours` | number |  |
| `userId` | string |  |
| `userImage` | string |  |
| `userName` | string |  |
| `userStatus` | string |  |
| `workingDays` | string |  |
| `workspaceId` | string |  |

## Native endpoint

Through the native Clockify API, this operation is `GET workspaces/:workspaceId/scheduling/assignments/users/:userId/totals` (base URL `https://api.clockify.me/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-workspace-user-capacity-total.md) for the provider-specific parameters and requirements.

