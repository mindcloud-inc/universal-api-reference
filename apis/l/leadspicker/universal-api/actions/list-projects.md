# Leadspicker: List Projects

Retrieves projects from Leadspicker.

```
GET https://connect.mindcloud.co/v1/universal/leadspicker/latest/actions/list-projects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Leadspicker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/leadspicker/latest/actions/list-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/leadspicker/latest/actions/list-projects?${params}`, {
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
| `searchQuery` | string | no | Search projects by name, labels, or contacts. |
| `limit` | number | no | Maximum number of projects to return. |
| `orderByField` | list<string> | no | Project ordering field: created, last_active, name, or pk. One of: `0`, `1`, `2`, `3`. Default: `pk`. |
| `orderDirection` | list<string> | no | Project ordering direction: asc or desc. One of: `0`, `1`. Default: `desc`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "auto_blacklist_same_email_domain_on_reply": true,
      "auto_enrich_emails": true,
      "created": "2026-05-07T12:00:00.000Z",
      "has_active_robots": true,
      "has_email_messages": true,
      "has_linkedin_messages": true,
      "has_robot_issue": true,
      "has_robots": true,
      "has_salesnav_messages": true,
      "id": 1,
      "is_allowed_to_send": true,
      "is_outreach_finished": true,
      "labels": [
        {}
      ],
      "last_active": "string",
      "name": "Ava Chen",
      "num_inbound_messages": 1,
      "paused": true,
      "paused_by_user": true,
      "paused_date": "string",
      "paused_reason": "string",
      "sending_in_progress": true,
      "stats": {},
      "use_global_blacklist": true,
      "user": 1,
      "user_email": "ava@example.com",
      "user_email_accounts": [
        {}
      ],
      "user_linkedin_account": {},
      "user_name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `auto_blacklist_same_email_domain_on_reply` | boolean |  |
| `auto_enrich_emails` | boolean |  |
| `created` | date |  |
| `has_active_robots` | boolean |  |
| `has_email_messages` | boolean |  |
| `has_linkedin_messages` | boolean |  |
| `has_robot_issue` | boolean |  |
| `has_robots` | boolean |  |
| `has_salesnav_messages` | boolean |  |
| `id` | number |  |
| `is_allowed_to_send` | boolean |  |
| `is_outreach_finished` | boolean |  |
| `labels` | array<object> |  |
| `last_active` | string |  |
| `name` | string |  |
| `num_inbound_messages` | number |  |
| `paused` | boolean |  |
| `paused_by_user` | boolean |  |
| `paused_date` | string |  |
| `paused_reason` | string |  |
| `sending_in_progress` | boolean |  |
| `stats` | object |  |
| `use_global_blacklist` | boolean |  |
| `user` | number |  |
| `user_email` | string |  |
| `user_email_accounts` | array<object> |  |
| `user_linkedin_account` | object |  |
| `user_name` | string |  |

## Native endpoint

Through the native Leadspicker API, this operation is `GET /app/sb/api/projects` (base URL `https://app.leadspicker.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-projects.md) for the provider-specific parameters and requirements.

