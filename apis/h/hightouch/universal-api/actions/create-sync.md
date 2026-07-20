# Hightouch: Create Sync

Creates a new sync in Hightouch.

```
POST https://connect.mindcloud.co/v1/universal/hightouch/latest/actions/create-sync
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hightouch `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/hightouch/latest/actions/create-sync" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "slug": "string",
  "configuration": {},
  "destinationId": 1,
  "modelId": 1,
  "schedule": {},
  "disabled": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hightouch/latest/actions/create-sync', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "slug": "string",
    "configuration": {},
    "destinationId": 1,
    "modelId": 1,
    "schedule": {},
    "disabled": true
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `slug` | string | yes | The sync slug. |
| `configuration` | object | yes | Sync configuration object. |
| `destinationId` | number | yes | Destination ID connected to the sync. |
| `modelId` | number | yes | Model ID connected to the sync. |
| `schedule` | object | yes | Sync schedule configuration object. |
| `disabled` | boolean | yes | Whether the sync is disabled. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "configuration": {},
      "createdAt": "2026-05-07T12:00:00.000Z",
      "destinationId": 1,
      "disabled": true,
      "externalSegment": {},
      "id": 1,
      "lastRunAt": "2026-05-07T12:00:00.000Z",
      "modelId": 1,
      "primaryKey": "string",
      "referencedColumns": [
        "string"
      ],
      "schedule": {},
      "slug": "string",
      "status": {},
      "tags": {},
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "workspaceId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `configuration` | object | Sync configuration. |
| `createdAt` | date | Creation timestamp. |
| `destinationId` | number | Destination ID. |
| `disabled` | boolean | Whether the sync is disabled. |
| `externalSegment` | object | External segment metadata. |
| `id` | number | Sync ID. |
| `lastRunAt` | date | Last run timestamp. |
| `modelId` | number | Model ID. |
| `primaryKey` | string | Sync primary key. |
| `referencedColumns` | array<string> | Referenced columns. |
| `schedule` | object | Sync schedule configuration. |
| `slug` | string | Sync slug. |
| `status` | object | Sync status. |
| `tags` | object | Sync tags. |
| `updatedAt` | date | Last update timestamp. |
| `workspaceId` | number | Workspace ID. |

## Native endpoint

Through the native Hightouch API, this operation is `POST /syncs` (base URL `https://api.hightouch.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-sync.md) for the provider-specific parameters and requirements.

