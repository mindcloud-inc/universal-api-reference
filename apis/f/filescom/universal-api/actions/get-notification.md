# Files.com: Get Notification

Finds a notification in Files.com by ID.

```
GET https://connect.mindcloud.co/v1/universal/filescom/latest/actions/get-notification
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Files.com `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/filescom/latest/actions/get-notification?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/filescom/latest/actions/get-notification?${params}`, {
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
| `id` | number | yes | Numeric notification ID. Default: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "group_id": 1,
      "group_name": "Ava Chen",
      "id": 1,
      "message": "string",
      "notify_on_download": true,
      "notify_on_upload": true,
      "path": "string",
      "recursive": true,
      "send_interval": "string",
      "user_id": 1,
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `group_id` | number |  |
| `group_name` | string |  |
| `id` | number |  |
| `message` | string |  |
| `notify_on_download` | boolean |  |
| `notify_on_upload` | boolean |  |
| `path` | string |  |
| `recursive` | boolean |  |
| `send_interval` | string |  |
| `user_id` | number |  |
| `username` | string |  |

## Native endpoint

Through the native Files.com API, this operation is `GET /notifications/:id` (base URL `{{credentials.siteUrl}}/api/rest/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-notification.md) for the provider-specific parameters and requirements.

