# Daytona: Create Sandbox

Creates a new sandbox in Daytona.

```
POST https://connect.mindcloud.co/v1/universal/daytona/latest/actions/create-sandbox
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Daytona `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/daytona/latest/actions/create-sandbox" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/daytona/latest/actions/create-sandbox', {
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

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | no | The name of the sandbox. |
| `snapshot` | string | no | The ID or name of the snapshot used for the sandbox. |
| `user` | string | no | User associated with the sandbox. |
| `target` | string | no | Target region where the sandbox will be created. |
| `class` | string | no | Sandbox class type. |
| `public` | boolean | no | Whether the sandbox HTTP preview is publicly accessible. |
| `cpu` | number | no | CPU cores allocated to the sandbox. |
| `gpu` | number | no | GPU units allocated to the sandbox. |
| `memory` | number | no | Memory allocated to the sandbox in GB. |
| `disk` | number | no | Disk space allocated to the sandbox in GB. |
| `autoStopInterval` | number | no | Auto-stop interval in minutes. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `env` | object | no | Environment variables for the sandbox. |
| `labels` | object | no | Labels for the sandbox. |
| `networkBlockAll` | boolean | no | Whether to block all network access for the sandbox. |
| `networkAllowList` | string | no | Comma-separated list of allowed CIDR network addresses. |
| `autoArchiveInterval` | number | no | Auto-archive interval in minutes. |
| `autoDeleteInterval` | number | no | Auto-delete interval in minutes. |
| `volumes[]` | array<object> | no | Volumes to attach to the sandbox. |
| `buildInfo` | object | no | Build information for the sandbox. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "autoStopInterval": 1,
      "cpu": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "desiredState": "string",
      "disk": 1,
      "env": {},
      "gpu": 1,
      "id": "string",
      "labels": {},
      "memory": 1,
      "name": "Ava Chen",
      "networkBlockAll": true,
      "organizationId": "string",
      "public": true,
      "runnerId": "string",
      "snapshot": "string",
      "state": "string",
      "target": "string",
      "toolboxProxyUrl": "https://example.com",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "user": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `autoStopInterval` | number |  |
| `cpu` | number |  |
| `createdAt` | date |  |
| `desiredState` | string |  |
| `disk` | number |  |
| `env` | object |  |
| `gpu` | number |  |
| `id` | string |  |
| `labels` | object |  |
| `memory` | number |  |
| `name` | string |  |
| `networkBlockAll` | boolean |  |
| `organizationId` | string |  |
| `public` | boolean |  |
| `runnerId` | string |  |
| `snapshot` | string |  |
| `state` | string |  |
| `target` | string |  |
| `toolboxProxyUrl` | string |  |
| `updatedAt` | date |  |
| `user` | string |  |

## Native endpoint

Through the native Daytona API, this operation is `POST /sandbox` (base URL `https://app.daytona.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-sandbox.md) for the provider-specific parameters and requirements.

