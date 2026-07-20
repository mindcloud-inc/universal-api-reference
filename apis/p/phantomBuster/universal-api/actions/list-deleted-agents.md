# PhantomBuster: List Deleted Agents

Retrieves deleted agents from PhantomBuster.

```
GET https://connect.mindcloud.co/v1/universal/phantomBuster/latest/actions/list-deleted-agents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PhantomBuster `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/phantomBuster/latest/actions/list-deleted-agents?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/phantomBuster/latest/actions/list-deleted-agents?${params}`, {
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
      "branch": "string",
      "createdAt": 1,
      "deletedAt": 1,
      "deletedBy": "string",
      "environment": "string",
      "id": "string",
      "lastEndedAt": 1,
      "lastEndType": "string",
      "lastExitCode": 1,
      "launchType": "string",
      "name": "Ava Chen",
      "nbContainersRunning": 1,
      "runningTime": 1,
      "s3Folder": "string",
      "script": "string",
      "scriptId": "string",
      "scriptOrgName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `branch` | string |  |
| `createdAt` | number |  |
| `deletedAt` | number |  |
| `deletedBy` | string |  |
| `environment` | string |  |
| `id` | string |  |
| `lastEndedAt` | number |  |
| `lastEndType` | string |  |
| `lastExitCode` | number |  |
| `launchType` | string |  |
| `name` | string |  |
| `nbContainersRunning` | number |  |
| `runningTime` | number |  |
| `s3Folder` | string |  |
| `script` | string |  |
| `scriptId` | string |  |
| `scriptOrgName` | string |  |

## Native endpoint

Through the native PhantomBuster API, this operation is `GET /agents/fetch-deleted` (base URL `https://api.phantombuster.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-deleted-agents.md) for the provider-specific parameters and requirements.

