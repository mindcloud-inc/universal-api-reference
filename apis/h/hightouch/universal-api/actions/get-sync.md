# Hightouch: Get Sync

Retrieves a sync from Hightouch.

```
GET https://connect.mindcloud.co/v1/universal/hightouch/latest/actions/get-sync
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hightouch `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hightouch/latest/actions/get-sync?connectionId=$CONNECTION_ID&syncId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "syncId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hightouch/latest/actions/get-sync?${params}`, {
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
| `syncId` | number | yes | The sync ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "destinationId": 1,
      "disabled": true,
      "id": 1,
      "modelId": 1,
      "slug": "string",
      "status": {},
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date | Creation timestamp. |
| `destinationId` | number | Destination ID. |
| `disabled` | boolean | Whether the sync is disabled. |
| `id` | number | Sync ID. |
| `modelId` | number | Model ID. |
| `slug` | string | Sync slug. |
| `status` | object | Sync status object. |
| `updatedAt` | date | Last update timestamp. |

## Native endpoint

Through the native Hightouch API, this operation is `GET /syncs/{syncId}` (base URL `https://api.hightouch.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-sync.md) for the provider-specific parameters and requirements.

