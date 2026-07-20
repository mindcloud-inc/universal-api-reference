# Cloud 66: List Stacks

Retrieves stacks from your Cloud 66 account.

```
GET https://connect.mindcloud.co/v1/universal/cloud66/latest/actions/list-stacks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloud 66 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloud66/latest/actions/list-stacks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloud66/latest/actions/list-stacks?${params}`, {
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
      "cloud": "string",
      "cloudStatus": "string",
      "createdAt": "string",
      "createdAtIso": "2026-05-07T12:00:00.000Z",
      "deployDirectory": "string",
      "environment": "string",
      "fqdn": "string",
      "framework": "string",
      "git": "string",
      "gitBranch": "string",
      "hasLoadbalancer": true,
      "health": 1,
      "language": "string",
      "lastActivity": "2026-05-07T12:00:00.000Z",
      "lastActivityIso": "2026-05-07T12:00:00.000Z",
      "maintenanceMode": true,
      "name": "Ava Chen",
      "redeployHook": "string",
      "status": 1,
      "uid": "string",
      "updatedAt": "string",
      "updatedAtIso": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cloud` | string |  |
| `cloudStatus` | string |  |
| `createdAt` | string |  |
| `createdAtIso` | date |  |
| `deployDirectory` | string |  |
| `environment` | string |  |
| `fqdn` | string |  |
| `framework` | string |  |
| `git` | string |  |
| `gitBranch` | string |  |
| `hasLoadbalancer` | boolean |  |
| `health` | number |  |
| `language` | string |  |
| `lastActivity` | date |  |
| `lastActivityIso` | date |  |
| `maintenanceMode` | boolean |  |
| `name` | string |  |
| `redeployHook` | string |  |
| `status` | number |  |
| `uid` | string |  |
| `updatedAt` | string |  |
| `updatedAtIso` | date |  |

## Native endpoint

Through the native Cloud 66 API, this operation is `GET /stacks` (base URL `https://app.cloud66.com/api/3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-stacks.md) for the provider-specific parameters and requirements.

