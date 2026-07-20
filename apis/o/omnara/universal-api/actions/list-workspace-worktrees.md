# Omnara: List Workspace Worktrees



```
GET https://connect.mindcloud.co/v1/universal/omnara/latest/actions/list-workspace-worktrees
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Omnara `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/omnara/latest/actions/list-workspace-worktrees?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/omnara/latest/actions/list-workspace-worktrees?${params}`, {
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
      "": [
        {
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
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `[]` | object |  |
| `[].checkpointMetadata` | object |  |
| `[].checkpointRestorePending` | boolean |  |
| `[].createdAt` | string |  |
| `[].currentCheckpointId` | string |  |
| `[].id` | string |  |
| `[].isMain` | boolean |  |
| `[].lastHeartbeatAt` | string |  |
| `[].lastSyncedCheckpointId` | string |  |
| `[].managedMachineId` | string |  |
| `[].name` | string |  |
| `[].path` | string |  |
| `[].updatedAt` | string |  |
| `[].userMachinePath` | object |  |
| `[].userMachinePath.id` | string |  |
| `[].userMachinePath.localPath` | string |  |
| `[].userMachinePath.machineId` | string |  |
| `[].workspaceId` | string |  |
| `[].worktreeType` | string |  |

## Native endpoint

Through the native Omnara API, this operation is `GET /api/v1/worktrees/workspace/{workspaceId}` (base URL `https://api.omnara.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-workspace-worktrees.md) for the provider-specific parameters and requirements.

