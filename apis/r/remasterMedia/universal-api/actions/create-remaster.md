# RemasterMedia: Create Remaster

Creates a remastered mediafile in RemasterMedia.

```
POST https://connect.mindcloud.co/v1/universal/remasterMedia/latest/actions/create-remaster
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RemasterMedia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/remasterMedia/latest/actions/create-remaster" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "source_id": "string",
  "options.preset": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/remasterMedia/latest/actions/create-remaster', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "source_id": "string",
    "options.preset": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `source_id` | string | yes | ID of the mediafile to remaster. |
| `options.preset` | string | yes | Remastering preset name. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `options.offset` | number | no | Optional number of seconds to skip from the start. |
| `options.duration` | number | no | Optional output duration limit in seconds. |
| `options.html5_compatible` | boolean | no | Whether to create HTML5-compatible output. |
| `webhook_url` | string | no | Optional webhook URL notified when processing finishes. |
| `user_data` | object | no | Optional custom object stored with the derived mediafile. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "mediafile": {
        "action": "string",
        "created_at": "2026-05-07T12:00:00.000Z",
        "expires_at": "2026-05-07T12:00:00.000Z",
        "id": "string",
        "metadata": {},
        "options": {},
        "status": "string",
        "updated_at": "2026-05-07T12:00:00.000Z",
        "url": "https://example.com",
        "user_data": {},
        "webhook_url": "https://example.com"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `mediafile` | object |  |
| `mediafile.action` | string |  |
| `mediafile.created_at` | date |  |
| `mediafile.expires_at` | date |  |
| `mediafile.id` | string |  |
| `mediafile.metadata` | object |  |
| `mediafile.options` | object |  |
| `mediafile.status` | string |  |
| `mediafile.updated_at` | date |  |
| `mediafile.url` | string |  |
| `mediafile.user_data` | object |  |
| `mediafile.webhook_url` | string |  |

## Native endpoint

Through the native RemasterMedia API, this operation is `POST /mediafiles/process` (base URL `https://api-sandbox.remastermedia.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-remaster.md) for the provider-specific parameters and requirements.

