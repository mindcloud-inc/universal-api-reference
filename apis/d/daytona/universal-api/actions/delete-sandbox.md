# Daytona: Delete Sandbox

Deletes an existing sandbox from Daytona.

```
DELETE https://connect.mindcloud.co/v1/universal/daytona/latest/actions/delete-sandbox
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Daytona `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/daytona/latest/actions/delete-sandbox?connectionId=$CONNECTION_ID&sandboxIdOrName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sandboxIdOrName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/daytona/latest/actions/delete-sandbox?${params}`, {
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
| `sandboxIdOrName` | string | yes | Sandbox ID or name. |

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

Through the native Daytona API, this operation is `DELETE /sandbox/[:sandboxIdOrName]` (base URL `https://app.daytona.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-sandbox.md) for the provider-specific parameters and requirements.

