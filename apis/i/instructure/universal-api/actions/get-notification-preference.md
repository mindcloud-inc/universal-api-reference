# Instructure: Get Notification Preference

Retrieves a notification preference from Instructure Canvas.

```
GET https://connect.mindcloud.co/v1/universal/instructure/latest/actions/get-notification-preference
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instructure `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/instructure/latest/actions/get-notification-preference?connectionId=$CONNECTION_ID&communicationChannelId=string&notification=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "communicationChannelId": "string",
  "notification": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/instructure/latest/actions/get-notification-preference?${params}`, {
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
| `communicationChannelId` | string | yes | The Canvas communication channel ID. |
| `notification` | string | yes | The Canvas notification code. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "notification_preferences": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `notification_preferences` | array<object> |  |

## Native endpoint

Through the native Instructure API, this operation is `GET /users/self/communication_channels/:communication_channel_id/notification_preferences/:notification` (base URL `https://canvas.instructure.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-notification-preference.md) for the provider-specific parameters and requirements.

