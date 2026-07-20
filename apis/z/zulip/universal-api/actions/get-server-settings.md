# Zulip: Get Server Settings

Retrieves current server settings from Zulip.

```
GET https://connect.mindcloud.co/v1/universal/zulip/latest/actions/get-server-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zulip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zulip/latest/actions/get-server-settings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zulip/latest/actions/get-server-settings?${params}`, {
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
      "authentication_methods": {},
      "email_auth_enabled": true,
      "external_authentication_methods": [
        {}
      ],
      "is_incompatible": true,
      "msg": "string",
      "push_notifications_enabled": true,
      "realm_description": "string",
      "realm_icon": "string",
      "realm_name": "Ava Chen",
      "realm_uri": "string",
      "realm_url": "https://example.com",
      "realm_web_public_access_enabled": true,
      "require_email_format_usernames": true,
      "result": "string",
      "zulip_feature_level": 1,
      "zulip_merge_base": "string",
      "zulip_version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `authentication_methods` | object |  |
| `email_auth_enabled` | boolean |  |
| `external_authentication_methods` | array<object> |  |
| `is_incompatible` | boolean |  |
| `msg` | string |  |
| `push_notifications_enabled` | boolean |  |
| `realm_description` | string |  |
| `realm_icon` | string |  |
| `realm_name` | string |  |
| `realm_uri` | string |  |
| `realm_url` | string |  |
| `realm_web_public_access_enabled` | boolean |  |
| `require_email_format_usernames` | boolean |  |
| `result` | string |  |
| `zulip_feature_level` | number |  |
| `zulip_merge_base` | string |  |
| `zulip_version` | string |  |

## Native endpoint

Through the native Zulip API, this operation is `GET /server_settings` (base URL `{{credentials.site}}/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-server-settings.md) for the provider-specific parameters and requirements.

