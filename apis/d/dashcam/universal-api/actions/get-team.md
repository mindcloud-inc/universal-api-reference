# Dashcam: Get Team

Retrieves team details from Dashcam.

```
GET https://connect.mindcloud.co/v1/universal/dashcam/latest/actions/get-team
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dashcam `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dashcam/latest/actions/get-team?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dashcam/latest/actions/get-team?${params}`, {
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
      "autoJoin": true,
      "autoJoinPossible": true,
      "createdAt": "string",
      "id": "string",
      "invite": {},
      "maxConcurrentSandboxes": 1,
      "maxUsers": 1,
      "name": "Ava Chen",
      "owner": {},
      "pendingInvites": [
        {}
      ],
      "plan": "string",
      "replayAccess": [
        {}
      ],
      "totalUsedSeconds": 1,
      "updatedAt": "string",
      "usageResetDate": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `autoJoin` | boolean |  |
| `autoJoinPossible` | boolean |  |
| `createdAt` | string |  |
| `id` | string |  |
| `invite` | object |  |
| `maxConcurrentSandboxes` | number |  |
| `maxUsers` | number |  |
| `name` | string |  |
| `owner` | object |  |
| `pendingInvites` | array<object> |  |
| `plan` | string |  |
| `replayAccess` | array<object> |  |
| `totalUsedSeconds` | number |  |
| `updatedAt` | string |  |
| `usageResetDate` | string |  |

## Native endpoint

Through the native Dashcam API, this operation is `GET /api/v1/teams` (base URL `https://api.testdriver.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-team.md) for the provider-specific parameters and requirements.

