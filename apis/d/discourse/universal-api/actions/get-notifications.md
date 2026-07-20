# Discourse: Get Notifications

Retrieves notifications for the current Discourse user.

```
GET https://connect.mindcloud.co/v1/universal/discourse/latest/actions/get-notifications
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Discourse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/discourse/latest/actions/get-notifications?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/discourse/latest/actions/get-notifications?${params}`, {
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
      "load_more_notifications": "string",
      "notifications": [
        {}
      ],
      "seen_notification_id": 1,
      "total_rows_notifications": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `load_more_notifications` | string |  |
| `notifications` | array<object> |  |
| `seen_notification_id` | number |  |
| `total_rows_notifications` | number |  |

## Native endpoint

Through the native Discourse API, this operation is `GET /notifications.json` (base URL `https://mindcloud.discourse.group`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-notifications.md) for the provider-specific parameters and requirements.

