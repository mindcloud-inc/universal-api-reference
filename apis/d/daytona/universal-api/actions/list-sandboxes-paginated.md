# Daytona: List Sandboxes Paginated

Retrieves a paginated list of sandboxes from Daytona.

```
GET https://connect.mindcloud.co/v1/universal/daytona/latest/actions/list-sandboxes-paginated
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Daytona `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/daytona/latest/actions/list-sandboxes-paginated?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/daytona/latest/actions/list-sandboxes-paginated?${params}`, {
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
| `id` | string | no | Filter by partial sandbox ID match. |
| `name` | string | no | Filter by partial sandbox name match. |
| `labels` | string | no | JSON encoded labels to filter by. |
| `includeErroredDeleted` | boolean | no | Include results with errored state and deleted desired state. |
| `states[]` | array<string> | no | List of states to filter by. |
| `snapshots[]` | array<string> | no | List of snapshot names to filter by. |
| `regions[]` | array<string> | no | List of regions to filter by. |
| `minCpu` | number | no | Minimum CPU. |
| `maxCpu` | number | no | Maximum CPU. |
| `minMemoryGiB` | number | no | Minimum memory in GiB. |
| `maxMemoryGiB` | number | no | Maximum memory in GiB. |
| `minDiskGiB` | number | no | Minimum disk space in GiB. |
| `maxDiskGiB` | number | no | Maximum disk space in GiB. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `lastEventAfter` | date | no | Include items with last event after this timestamp. |
| `lastEventBefore` | date | no | Include items with last event before this timestamp. |

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

Through the native Daytona API, this operation is `GET /sandbox/paginated` (base URL `https://app.daytona.io/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-sandboxes-paginated.md) for the provider-specific parameters and requirements.

