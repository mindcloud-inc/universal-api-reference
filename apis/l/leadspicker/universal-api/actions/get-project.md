# Leadspicker: Get Project

Retrieves a project from Leadspicker.

```
GET https://connect.mindcloud.co/v1/universal/leadspicker/latest/actions/get-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Leadspicker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/leadspicker/latest/actions/get-project?connectionId=$CONNECTION_ID&projectId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/leadspicker/latest/actions/get-project?${params}`, {
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
| `projectId` | number | yes | Leadspicker project identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "allow_showcase": true,
      "auto_blacklist_same_email_domain_on_reply": true,
      "auto_enrich_emails": true,
      "created": "2026-05-07T12:00:00.000Z",
      "has_active_robots": true,
      "has_email_messages": true,
      "has_linkedin_messages": true,
      "has_missing_variables": true,
      "has_robot_issue": true,
      "has_robots": true,
      "has_salesnav_messages": true,
      "headers_data": [
        {}
      ],
      "id": 1,
      "is_allowed_to_send": true,
      "is_outreach_finished": true,
      "labels": [
        {}
      ],
      "lead_hunter_status": {},
      "name": "Ava Chen",
      "paused": true,
      "paused_by_user": true,
      "paused_date": "string",
      "paused_reason": "string",
      "progress_data": [
        {}
      ],
      "sending_in_progress": true,
      "sequence_setting": {},
      "stats": {},
      "undefined_variables": [
        "string"
      ],
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
| `allow_showcase` | boolean |  |
| `auto_blacklist_same_email_domain_on_reply` | boolean |  |
| `auto_enrich_emails` | boolean |  |
| `created` | date |  |
| `has_active_robots` | boolean |  |
| `has_email_messages` | boolean |  |
| `has_linkedin_messages` | boolean |  |
| `has_missing_variables` | boolean |  |
| `has_robot_issue` | boolean |  |
| `has_robots` | boolean |  |
| `has_salesnav_messages` | boolean |  |
| `headers_data` | array<object> |  |
| `id` | number |  |
| `is_allowed_to_send` | boolean |  |
| `is_outreach_finished` | boolean |  |
| `labels` | array<object> |  |
| `lead_hunter_status` | object |  |
| `name` | string |  |
| `paused` | boolean |  |
| `paused_by_user` | boolean |  |
| `paused_date` | string |  |
| `paused_reason` | string |  |
| `progress_data` | array<object> |  |
| `sending_in_progress` | boolean |  |
| `sequence_setting` | object |  |
| `stats` | object |  |
| `undefined_variables` | array<string> |  |
| `use_global_blacklist` | boolean |  |
| `user` | number |  |
| `user_email` | string |  |
| `user_email_accounts` | array<object> |  |
| `user_linkedin_account` | object |  |
| `user_name` | string |  |

## Native endpoint

Through the native Leadspicker API, this operation is `GET /app/sb/api/projects/:project_id` (base URL `https://app.leadspicker.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project.md) for the provider-specific parameters and requirements.

