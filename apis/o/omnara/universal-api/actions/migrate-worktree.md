# Omnara: Migrate Worktree



```
PUT https://connect.mindcloud.co/v1/universal/omnara/latest/actions/migrate-worktree
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Omnara `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/omnara/latest/actions/migrate-worktree" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/omnara/latest/actions/migrate-worktree', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "status": "string",
      "worktree": {
        "checkpointMetadata": {},
        "checkpointRestorePending": true,
        "createdAt": "string",
        "currentCheckpointId": "string",
        "id": "string",
        "isMain": true,
        "lastHeartbeatAt": "string",
        "lastSyncedCheckpointId": "string",
        "managedMachineId": "string",
        "name": "Ava Chen",
        "path": "string",
        "updatedAt": "string",
        "userMachinePath": {
          "id": "string",
          "localPath": "string",
          "machineId": "string"
        },
        "workspaceId": "string",
        "worktreeType": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | string |  |
| `worktree` | object |  |
| `worktree.checkpointMetadata` | object |  |
| `worktree.checkpointRestorePending` | boolean |  |
| `worktree.createdAt` | string |  |
| `worktree.currentCheckpointId` | string |  |
| `worktree.id` | string |  |
| `worktree.isMain` | boolean |  |
| `worktree.lastHeartbeatAt` | string |  |
| `worktree.lastSyncedCheckpointId` | string |  |
| `worktree.managedMachineId` | string |  |
| `worktree.name` | string |  |
| `worktree.path` | string |  |
| `worktree.updatedAt` | string |  |
| `worktree.userMachinePath` | object |  |
| `worktree.userMachinePath.id` | string |  |
| `worktree.userMachinePath.localPath` | string |  |
| `worktree.userMachinePath.machineId` | string |  |
| `worktree.workspaceId` | string |  |
| `worktree.worktreeType` | string |  |

## Native endpoint

Through the native Omnara API, this operation is `POST /api/v1/worktrees/{worktreeId}/migrate` (base URL `https://api.omnara.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/migrate-worktree.md) for the provider-specific parameters and requirements.

