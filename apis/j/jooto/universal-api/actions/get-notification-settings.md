# Jooto: Get Notification Settings



```
GET https://connect.mindcloud.co/v1/universal/jooto/latest/actions/get-notification-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jooto `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jooto/latest/actions/get-notification-settings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jooto/latest/actions/get-notification-settings?${params}`, {
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
      "enabled": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `enabled` | boolean | Whether the notification setting is enabled. |

## Native endpoint

Through the native Jooto API, this operation is `GET /api/v1/notifications/get_settings` (base URL `https://app.jooto.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-notification-settings.md) for the provider-specific parameters and requirements.

