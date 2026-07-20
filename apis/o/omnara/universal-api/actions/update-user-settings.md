# Omnara: Update User Settings



```
PUT https://connect.mindcloud.co/v1/universal/omnara/latest/actions/update-user-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Omnara `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/omnara/latest/actions/update-user-settings" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/omnara/latest/actions/update-user-settings', {
  method: 'PUT',
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
      "code": {
        "defaultProvider": "string",
        "mode": "string",
        "providers": {
          "claudeCode": {
            "model": "string"
          },
          "codex": {
            "model": "string",
            "thinking": "string"
          }
        }
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
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | object |  |
| `code.defaultProvider` | string |  |
| `code.mode` | string |  |
| `code.providers` | object |  |
| `code.providers.claudeCode` | object |  |
| `code.providers.claudeCode.model` | string |  |
| `code.providers.codex` | object |  |
| `code.providers.codex.model` | string |  |
| `code.providers.codex.thinking` | string |  |
| `git` | object |  |
| `git.defaultWorktreeMode` | string |  |
| `notifications` | object |  |
| `notifications.email` | object |  |
| `notifications.email.enabled` | boolean |  |
| `notifications.email.notificationEmail` | string |  |
| `notifications.mobile` | object |  |
| `notifications.mobile.mode` | string |  |
| `notifications.sms` | object |  |
| `notifications.sms.enabled` | boolean |  |
| `notifications.sms.phoneNumber` | string |  |
| `voice` | object |  |
| `voice.language` | string |  |

## Native endpoint

Through the native Omnara API, this operation is `PATCH /api/v1/user/settings` (base URL `https://api.omnara.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-user-settings.md) for the provider-specific parameters and requirements.

