# Svix: Expunge All Message Contents

Deletes all message payloads from a Svix application.

```
POST https://connect.mindcloud.co/v1/universal/svix/latest/actions/expunge-all-message-contents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Svix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/svix/latest/actions/expunge-all-message-contents" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/svix/latest/actions/expunge-all-message-contents', {
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



## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "status": "string",
      "task": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `status` | string |  |
| `task` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Svix API, this operation is `POST /api/v1/app/{app_id}/msg/expunge-all-contents` (base URL `https://api.us.svix.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/expunge-all-message-contents.md) for the provider-specific parameters and requirements.

