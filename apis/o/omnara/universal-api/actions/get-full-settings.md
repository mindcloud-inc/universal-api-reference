# Omnara: Get Full Settings



```
GET https://connect.mindcloud.co/v1/universal/omnara/latest/actions/get-full-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Omnara `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/omnara/latest/actions/get-full-settings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/omnara/latest/actions/get-full-settings?${params}`, {
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
      "code": {
        "defaultProvider": "string",
        "mode": "string"
      },
      "git": {
        "defaultWorktreeMode": "string"
      },
      "notifications": {
        "email": {
          "enabled": true,
          "notificationEmail": "ava@example.com"
        },
        "mobile": {
          "mode": "string"
        },
        "sms": {
          "enabled": true,
          "phoneNumber": "string"
        }
      },
      "voice": {
        "language": "string"
      },
      "welcomeEmailSentAt": "ava@example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code.defaultProvider` | string |  |
| `code.mode` | string |  |
| `git.defaultWorktreeMode` | string |  |
| `notifications.email.enabled` | boolean |  |
| `notifications.email.notificationEmail` | string |  |
| `notifications.mobile.mode` | string |  |
| `notifications.sms.enabled` | boolean |  |
| `notifications.sms.phoneNumber` | string |  |
| `voice.language` | string |  |
| `welcomeEmailSentAt` | string |  |

## Native endpoint

Through the native Omnara API, this operation is `GET /api/v1/user/settings` (base URL `https://api.omnara.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-full-settings.md) for the provider-specific parameters and requirements.

