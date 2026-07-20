# Hightouch: Trigger Sync

Triggers a sync run in Hightouch.

```
POST https://connect.mindcloud.co/v1/universal/hightouch/latest/actions/trigger-sync
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hightouch `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/hightouch/latest/actions/trigger-sync" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "syncId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hightouch/latest/actions/trigger-sync', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "syncId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `syncId` | string | yes | The sync ID. |
| `clearAndFill` | boolean | no | Whether to clear and fill when triggering the sync. |
| `resetCDC` | boolean | no | Whether to reset change data capture when triggering the sync. |
| `fullResync` | boolean | no | Whether to trigger a full resync. |

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

Through the native Hightouch API, this operation is `POST /syncs/{syncId}/trigger` (base URL `https://api.hightouch.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/trigger-sync.md) for the provider-specific parameters and requirements.

