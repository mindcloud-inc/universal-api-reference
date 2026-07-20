# Leadspicker: List LinkedIn Accounts

Retrieves LinkedIn accounts from Leadspicker.

```
GET https://connect.mindcloud.co/v1/universal/leadspicker/latest/actions/list-linkedin-accounts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Leadspicker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/leadspicker/latest/actions/list-linkedin-accounts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/leadspicker/latest/actions/list-linkedin-accounts?${params}`, {
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
      "browser_url": "https://example.com",
      "cookies_updated": "string",
      "daily_connection_limit": 1,
      "daily_connection_limit_remaining": 1,
      "daily_event_invite_limit": 1,
      "daily_event_invite_limit_remaining": 1,
      "daily_follow_limit": 1,
      "daily_follow_limit_remaining": 1,
      "daily_inmail_limit": 1,
      "daily_inmail_limit_remaining": 1,
      "daily_message_limit": 1,
      "daily_message_limit_remaining": 1,
      "daily_visit_limit": 1,
      "has_context": true,
      "has_credentials": true,
      "id": 1,
      "is_disabled": true,
      "is_premium": true,
      "is_revoked": true,
      "labels": [
        {}
      ],
      "linkedin_id": "https://example.com",
      "linkedin_name": "https://example.com",
      "linkedin_session_connected": true,
      "my_profile_url": "https://example.com",
      "proxy_country": "string",
      "recruiter_session_connected": true,
      "sales_nav_session_connected": true,
      "user": 1,
      "user_email": "ava@example.com",
      "user_name": "Ava Chen",
      "weekly_invitations_limit_exceeded": true,
      "withdraw_after_days": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `browser_url` | string |  |
| `cookies_updated` | string |  |
| `daily_connection_limit` | number |  |
| `daily_connection_limit_remaining` | number |  |
| `daily_event_invite_limit` | number |  |
| `daily_event_invite_limit_remaining` | number |  |
| `daily_follow_limit` | number |  |
| `daily_follow_limit_remaining` | number |  |
| `daily_inmail_limit` | number |  |
| `daily_inmail_limit_remaining` | number |  |
| `daily_message_limit` | number |  |
| `daily_message_limit_remaining` | number |  |
| `daily_visit_limit` | number |  |
| `has_context` | boolean |  |
| `has_credentials` | boolean |  |
| `id` | number |  |
| `is_disabled` | boolean |  |
| `is_premium` | boolean |  |
| `is_revoked` | boolean |  |
| `labels` | array<object> |  |
| `linkedin_id` | string |  |
| `linkedin_name` | string |  |
| `linkedin_session_connected` | boolean |  |
| `my_profile_url` | string |  |
| `proxy_country` | string |  |
| `recruiter_session_connected` | boolean |  |
| `sales_nav_session_connected` | boolean |  |
| `user` | number |  |
| `user_email` | string |  |
| `user_name` | string |  |
| `weekly_invitations_limit_exceeded` | boolean |  |
| `withdraw_after_days` | number |  |

## Native endpoint

Through the native Leadspicker API, this operation is `GET /app/sb/api/linkedin-accounts` (base URL `https://app.leadspicker.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-linkedin-accounts.md) for the provider-specific parameters and requirements.

