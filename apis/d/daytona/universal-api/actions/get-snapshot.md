# Daytona: Get Snapshot

Retrieves snapshot details from Daytona.

```
GET https://connect.mindcloud.co/v1/universal/daytona/latest/actions/get-snapshot
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Daytona `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/daytona/latest/actions/get-snapshot?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/daytona/latest/actions/get-snapshot?${params}`, {
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
| `id` | string | yes | Snapshot ID or name. |

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

Through the native Daytona API, this operation is `GET /snapshots/[:id]` (base URL `https://app.daytona.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-snapshot.md) for the provider-specific parameters and requirements.

