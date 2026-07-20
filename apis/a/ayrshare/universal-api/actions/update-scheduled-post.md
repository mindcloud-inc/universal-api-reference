# Ayrshare: Update Scheduled Post

Updates a scheduled post in Ayrshare.

```
PUT https://connect.mindcloud.co/v1/universal/ayrshare/latest/actions/update-scheduled-post
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ayrshare `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/ayrshare/latest/actions/update-scheduled-post" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ayrshare/latest/actions/update-scheduled-post', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Ayrshare scheduled post ID to update. |
| `scheduleDate` | date | no | New UTC ISO 8601 schedule date for the pending scheduled post. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `scheduledPause` | boolean | no | Pause or unpause a scheduled post. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "message": "string",
      "scheduleDate": "2026-05-07T12:00:00.000Z",
      "scheduledPaused": true,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Ayrshare Post ID. |
| `message` | string | Status or error message. |
| `scheduleDate` | date | Updated schedule date. |
| `scheduledPaused` | boolean | Whether the scheduled post is paused. |
| `status` | string | Update status. |

## Native endpoint

Through the native Ayrshare API, this operation is `PATCH /post` (base URL `https://api.ayrshare.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-scheduled-post.md) for the provider-specific parameters and requirements.

