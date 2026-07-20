# Hightouch: Update Sync

Updates an existing sync in Hightouch.

```
PUT https://connect.mindcloud.co/v1/universal/hightouch/latest/actions/update-sync
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hightouch `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/hightouch/latest/actions/update-sync" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "syncId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hightouch/latest/actions/update-sync', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "syncId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `syncId` | number | yes | The sync ID. |
| `configuration` | object | no | Sync configuration object. |
| `schedule` | object | no | Sync schedule configuration object. |
| `disabled` | boolean | no | Whether the sync is disabled. |

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

Through the native Hightouch API, this operation is `PATCH /syncs/{syncId}` (base URL `https://api.hightouch.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-sync.md) for the provider-specific parameters and requirements.

