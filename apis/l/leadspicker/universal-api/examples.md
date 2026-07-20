# Leadspicker Universal API Examples

These examples use the MindCloud API key and Leadspicker connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current User Info

Retrieves current user information from Leadspicker.

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

Example response:

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

See the full [Get Current User Info action reference](actions/get-current-user-info.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/leadspicker/latest/actions/get-current-user-info).
