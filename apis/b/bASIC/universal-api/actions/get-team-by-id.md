# BASIC: Get team by ID

Retrieves a team by ID from BASIC.

```
GET https://connect.mindcloud.co/v1/universal/bASIC/latest/actions/get-team-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BASIC `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bASIC/latest/actions/get-team-by-id?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bASIC/latest/actions/get-team-by-id?${params}`, {
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
      "data": {
        "created_at": "2026-05-07T12:00:00.000Z",
        "id": "string",
        "invites": [
          {
            "email_or_username": "ava@example.com",
            "id": "string",
            "role_name": "Ava Chen",
            "roles": "string",
            "team_id": "string"
          }
        ],
        "members": [
          {
            "account_id": "string",
            "role_name": "Ava Chen",
            "roles": "string"
          }
        ],
        "name": "Ava Chen",
        "owner_id": "string",
        "projects": [
          {
            "id": "string",
            "name": "Ava Chen",
            "profile": {
              "icon_url": "https://example.com"
            },
            "slug": "string"
          }
        ],
        "slug": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.created_at` | date |  |
| `data.id` | string |  |
| `data.invites[].email_or_username` | string |  |
| `data.invites[].id` | string |  |
| `data.invites[].role_name` | string |  |
| `data.invites[].roles` | string |  |
| `data.invites[].team_id` | string |  |
| `data.members[].account_id` | string |  |
| `data.members[].role_name` | string |  |
| `data.members[].roles` | string |  |
| `data.name` | string |  |
| `data.owner_id` | string |  |
| `data.projects[].id` | string |  |
| `data.projects[].name` | string |  |
| `data.projects[].profile.icon_url` | string |  |
| `data.projects[].slug` | string |  |
| `data.slug` | string |  |

## Native endpoint

Through the native BASIC API, this operation is `GET /team/{team_id}` (base URL `https://api.basic.tech`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-team-by-id.md) for the provider-specific parameters and requirements.

