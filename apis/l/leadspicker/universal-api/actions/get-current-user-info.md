# Leadspicker: Get Current User Info

Retrieves current user information from Leadspicker.

```
GET https://connect.mindcloud.co/v1/universal/leadspicker/latest/actions/get-current-user-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Leadspicker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/leadspicker/latest/actions/get-current-user-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/leadspicker/latest/actions/get-current-user-info?${params}`, {
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
      "config": {},
      "created_magic_column_count": 1,
      "created_robots_count": 1,
      "csrf_token": "string",
      "customer": {},
      "daily_scraped_leads": 1,
      "date_joined": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "fair_usage": {},
      "first_name": "Ava",
      "free_trial_days_left": 1,
      "has_active_subscription": true,
      "has_free_trial": true,
      "id": 1,
      "is_authenticated": true,
      "last_name": "Chen",
      "organization": {},
      "organization_invitations": [
        {}
      ],
      "recommended_daily_scraping_limit": 1,
      "should_have_access_to_paid_features": true,
      "subscription": {},
      "websocket_group": "string",
      "workspace_context": {},
      "workspace_invitations": [
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
| `config` | object |  |
| `created_magic_column_count` | number |  |
| `created_robots_count` | number |  |
| `csrf_token` | string |  |
| `customer` | object |  |
| `daily_scraped_leads` | number |  |
| `date_joined` | date |  |
| `email` | string |  |
| `fair_usage` | object |  |
| `first_name` | string |  |
| `free_trial_days_left` | number |  |
| `has_active_subscription` | boolean |  |
| `has_free_trial` | boolean |  |
| `id` | number |  |
| `is_authenticated` | boolean |  |
| `last_name` | string |  |
| `organization` | object |  |
| `organization_invitations` | array<object> |  |
| `recommended_daily_scraping_limit` | number |  |
| `should_have_access_to_paid_features` | boolean |  |
| `subscription` | object |  |
| `websocket_group` | string |  |
| `workspace_context` | object |  |
| `workspace_invitations` | array<object> |  |

## Native endpoint

Through the native Leadspicker API, this operation is `GET /app/sb/api/auth/me` (base URL `https://app.leadspicker.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-user-info.md) for the provider-specific parameters and requirements.

