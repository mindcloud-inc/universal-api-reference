# Daytona: Create Snapshot

Creates a new snapshot in Daytona.

```
POST https://connect.mindcloud.co/v1/universal/daytona/latest/actions/create-snapshot
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Daytona `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/daytona/latest/actions/create-snapshot" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/daytona/latest/actions/create-snapshot', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | The name of the snapshot. |
| `imageName` | string | no | The image name of the snapshot. |
| `entrypoint[]` | array<string> | no | Entrypoint command for the snapshot. |
| `cpu` | number | no | CPU cores allocated to the resulting sandbox. |
| `gpu` | number | no | GPU units allocated to the resulting sandbox. |
| `memory` | number | no | Memory allocated to the resulting sandbox in GB. |
| `disk` | number | no | Disk space allocated to the sandbox in GB. |
| `regionId` | string | no | ID of the region where the snapshot will be available. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `buildInfo` | object | no | Build information for the snapshot. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cpu": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "disk": 1,
      "entrypoint": [
        "string"
      ],
      "errorReason": "string",
      "general": true,
      "gpu": 1,
      "id": "string",
      "imageName": "Ava Chen",
      "initialRunnerId": "string",
      "lastUsedAt": "2026-05-07T12:00:00.000Z",
      "mem": 1,
      "name": "Ava Chen",
      "organizationId": "string",
      "ref": "string",
      "regionIds": [
        "string"
      ],
      "size": 1,
      "state": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cpu` | number |  |
| `createdAt` | date |  |
| `disk` | number |  |
| `entrypoint` | array<string> |  |
| `errorReason` | string |  |
| `general` | boolean |  |
| `gpu` | number |  |
| `id` | string |  |
| `imageName` | string |  |
| `initialRunnerId` | string |  |
| `lastUsedAt` | date |  |
| `mem` | number |  |
| `name` | string |  |
| `organizationId` | string |  |
| `ref` | string |  |
| `regionIds` | array<string> |  |
| `size` | number |  |
| `state` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Daytona API, this operation is `POST /snapshots` (base URL `https://app.daytona.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-snapshot.md) for the provider-specific parameters and requirements.

