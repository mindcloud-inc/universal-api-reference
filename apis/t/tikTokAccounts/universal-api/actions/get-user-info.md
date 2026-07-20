# TikTok Accounts: Get User Info

Retrieves profile information for the authenticated user in TikTok.

```
GET https://connect.mindcloud.co/v1/universal/tikTokAccounts/latest/actions/get-user-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TikTok Accounts `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tikTokAccounts/latest/actions/get-user-info?connectionId=$CONNECTION_ID&fields=open_id%2Cavatar_url%2Cdisplay_name" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fields": "open_id,avatar_url,display_name"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tikTokAccounts/latest/actions/get-user-info?${params}`, {
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
| `fields` | string | yes | Comma-separated TikTok user fields to return. The default includes only fields authorized by user.info.basic. Default: `open_id,union_id,avatar_url,avatar_url_100,avatar_large_url,display_name`. Example: `open_id,avatar_url,display_name`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "avatar_large_url": "https://example.com",
      "avatar_url": "https://example.com",
      "avatar_url_100": "https://example.com",
      "display_name": "Ava Chen",
      "open_id": "string",
      "union_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `avatar_large_url` | string | Higher resolution user profile image URL. |
| `avatar_url` | string | User profile image URL. |
| `avatar_url_100` | string | User profile image URL in 100x100 size. |
| `display_name` | string | User profile display name. |
| `open_id` | string | Unique identification of the user in the current application. |
| `union_id` | string | Unique identification of the user across apps for the same developer. |

## Native endpoint

Through the native TikTok Accounts API, this operation is `GET /v2/user/info/` (base URL `https://open.tiktokapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-info.md) for the provider-specific parameters and requirements.

