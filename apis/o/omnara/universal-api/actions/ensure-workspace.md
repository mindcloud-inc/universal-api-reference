# Omnara: Ensure Workspace



```
POST https://connect.mindcloud.co/v1/universal/omnara/latest/actions/ensure-workspace
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Omnara `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/omnara/latest/actions/ensure-workspace" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/omnara/latest/actions/ensure-workspace', {
  method: 'POST',
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
      "createdAt": "string",
      "gitHost": "string",
      "gitPath": "string",
      "id": "string",
      "updatedAt": "string",
      "userId": "string",
      "userMachinePaths": [
        {
          "localPath": "string",
          "userMachineId": "string"
        }
      ],
      "workspaceConfig": {
        "git": {
          "baseRef": "string",
          "remote": "string"
        },
        "remoteEnv": {
          "env": [
            {}
          ]
        },
        "setup": {
          "script": "string"
        },
        "sync": {
          "enabled": true
        }
      },
      "workspaceMetadata": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `gitHost` | string |  |
| `gitPath` | string |  |
| `id` | string |  |
| `updatedAt` | string |  |
| `userId` | string |  |
| `userMachinePaths` | array<object> |  |
| `userMachinePaths[]` | object |  |
| `userMachinePaths[].localPath` | string |  |
| `userMachinePaths[].userMachineId` | string |  |
| `workspaceConfig` | object |  |
| `workspaceConfig.git` | object |  |
| `workspaceConfig.git.baseRef` | string |  |
| `workspaceConfig.git.remote` | string |  |
| `workspaceConfig.remoteEnv` | object |  |
| `workspaceConfig.remoteEnv.env` | array<object> |  |
| `workspaceConfig.remoteEnv.env[]` | object |  |
| `workspaceConfig.setup` | object |  |
| `workspaceConfig.setup.script` | string |  |
| `workspaceConfig.sync` | object |  |
| `workspaceConfig.sync.enabled` | boolean |  |
| `workspaceMetadata` | object |  |

## Native endpoint

Through the native Omnara API, this operation is `POST /api/v1/workspaces/ensure` (base URL `https://api.omnara.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/ensure-workspace.md) for the provider-specific parameters and requirements.

