# Unstructured: Get Unread Notification Count

Retrieves the unread notification count from Unstructured.

```
GET https://connect.mindcloud.co/v1/universal/unstructured/latest/actions/get-unread-notification-count
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Unstructured `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/unstructured/latest/actions/get-unread-notification-count?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/unstructured/latest/actions/get-unread-notification-count?${params}`, {
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
      "unreadCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `unreadCount` | number | Unread notification count. |

## Native endpoint

Through the native Unstructured API, this operation is `GET /notifications/unread-count` (base URL `https://platform.unstructuredapp.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-unread-notification-count.md) for the provider-specific parameters and requirements.

