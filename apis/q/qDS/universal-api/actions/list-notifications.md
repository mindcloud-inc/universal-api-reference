# QDS: List Notifications



```
GET https://connect.mindcloud.co/v1/universal/qDS/latest/actions/list-notifications
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QDS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/qDS/latest/actions/list-notifications?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/qDS/latest/actions/list-notifications?${params}`, {
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
      "notifications": [
        {
          "created_at": "2026-05-07T12:00:00.000Z",
          "id": 1,
          "post_content": "string",
          "post_title": "string",
          "show_on": "2026-05-07T12:00:00.000Z",
          "updated_at": "2026-05-07T12:00:00.000Z",
          "user_id": 1
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `notifications[].created_at` | date |  |
| `notifications[].id` | number |  |
| `notifications[].post_content` | string |  |
| `notifications[].post_title` | string |  |
| `notifications[].show_on` | date |  |
| `notifications[].updated_at` | date |  |
| `notifications[].user_id` | number |  |

## Native endpoint

Through the native QDS API, this operation is `GET /notifications` (base URL `https://qdsapp.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-notifications.md) for the provider-specific parameters and requirements.

