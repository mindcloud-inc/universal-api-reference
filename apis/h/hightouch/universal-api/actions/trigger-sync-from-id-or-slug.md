# Hightouch: Trigger Sync From ID or Slug

Triggers a sync run in Hightouch by ID or slug.

```
POST https://connect.mindcloud.co/v1/universal/hightouch/latest/actions/trigger-sync-from-id-or-slug
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hightouch `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/hightouch/latest/actions/trigger-sync-from-id-or-slug" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hightouch/latest/actions/trigger-sync-from-id-or-slug', {
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
| `syncSlug` | string | no | Sync slug to trigger. |
| `syncId` | string | no | Sync ID to trigger. |
| `fullResync` | boolean | no | Whether to trigger a full resync. |
| `clearAndFill` | boolean | no | Whether to clear and fill when triggering the sync. |
| `resetCDC` | boolean | no | Whether to reset change data capture when triggering the sync. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Triggered sync run ID. |

## Native endpoint

Through the native Hightouch API, this operation is `POST /syncs/trigger` (base URL `https://api.hightouch.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/trigger-sync-from-id-or-slug.md) for the provider-specific parameters and requirements.

