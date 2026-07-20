# Daytona: Recover Sandbox

Recovers a sandbox from an error state in Daytona.

```
PUT https://connect.mindcloud.co/v1/universal/daytona/latest/actions/recover-sandbox
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Daytona `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/daytona/latest/actions/recover-sandbox" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "sandboxIdOrName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/daytona/latest/actions/recover-sandbox', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "sandboxIdOrName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sandboxIdOrName` | string | yes | ID or name of the sandbox. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "autoArchiveInterval": 1,
      "autoDeleteInterval": 1,
      "autoStopInterval": 1,
      "backupCreatedAt": "2026-05-07T12:00:00.000Z",
      "backupState": "string",
      "buildInfo": {},
      "class": "string",
      "cpu": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "daemonVersion": "string",
      "desiredState": "string",
      "disk": 1,
      "env": {},
      "errorReason": "string",
      "gpu": 1,
      "id": "string",
      "labels": {},
      "memory": 1,
      "name": "Ava Chen",
      "networkAllowList": "string",
      "networkBlockAll": true,
      "organizationId": "string",
      "public": true,
      "recoverable": true,
      "runnerId": "string",
      "snapshot": "string",
      "state": "string",
      "target": "string",
      "toolboxProxyUrl": "https://example.com",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "user": "string",
      "volumes": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `autoArchiveInterval` | number | Auto-archive interval in minutes. |
| `autoDeleteInterval` | number | Auto-delete interval in minutes. |
| `autoStopInterval` | number | Auto-stop interval in minutes. |
| `backupCreatedAt` | date | The creation timestamp of the last backup. |
| `backupState` | string | The backup state. |
| `buildInfo` | object | Build information for the sandbox. |
| `class` | string | The class of the sandbox. |
| `cpu` | number | The CPU quota for the sandbox. |
| `createdAt` | date | The creation timestamp of the sandbox. |
| `daemonVersion` | string | The daemon version running in the sandbox. |
| `desiredState` | string | The desired sandbox state. |
| `disk` | number | The disk quota for the sandbox. |
| `env` | object | Environment variables for the sandbox. |
| `errorReason` | string | The sandbox error reason. |
| `gpu` | number | The GPU quota for the sandbox. |
| `id` | string | The ID of the sandbox. |
| `labels` | object | Labels for the sandbox. |
| `memory` | number | The memory quota for the sandbox. |
| `name` | string | The name of the sandbox. |
| `networkAllowList` | string | Comma-separated allowed CIDR network addresses. |
| `networkBlockAll` | boolean | Whether network access is blocked for the sandbox. |
| `organizationId` | string | The organization ID of the sandbox. |
| `public` | boolean | Whether the sandbox HTTP preview is public. |
| `recoverable` | boolean | Whether the sandbox error is recoverable. |
| `runnerId` | string | The runner ID of the sandbox. |
| `snapshot` | string | The snapshot used for the sandbox. |
| `state` | string | The current sandbox state. |
| `target` | string | The target environment for the sandbox. |
| `toolboxProxyUrl` | string | The toolbox proxy URL for the sandbox. |
| `updatedAt` | date | The last update timestamp of the sandbox. |
| `user` | string | The user associated with the sandbox. |
| `volumes` | array<object> | Volumes attached to the sandbox. |

## Native endpoint

Through the native Daytona API, this operation is `POST /sandbox/[:sandboxIdOrName]/recover` (base URL `https://app.daytona.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/recover-sandbox.md) for the provider-specific parameters and requirements.

