# Socialbu: Get Notification

Retrieves a notification by ID from SocialBu.

```
GET https://connect.mindcloud.co/v1/universal/socialbu/latest/actions/get-notification
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Socialbu `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/socialbu/latest/actions/get-notification?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/socialbu/latest/actions/get-notification?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "string",
      "id": 1,
      "message": "string",
      "read": true,
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | string |  |
| `id` | number |  |
| `message` | string |  |
| `read` | boolean |  |
| `title` | string |  |

## Native endpoint

Through the native Socialbu API, this operation is `GET /notifications/{id}` (base URL `https://socialbu.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-notification.md) for the provider-specific parameters and requirements.

