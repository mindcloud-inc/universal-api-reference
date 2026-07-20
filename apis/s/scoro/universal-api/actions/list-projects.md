# Scoro: List Projects

Retrieves projects from Scoro.

```
GET https://connect.mindcloud.co/v1/universal/scoro/latest/actions/list-projects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scoro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scoro/latest/actions/list-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scoro/latest/actions/list-projects?${params}`, {
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
      "account_id": "string",
      "budget_type": "string",
      "color": "string",
      "company_id": 1,
      "company_name": "Ava Chen",
      "date": "string",
      "deadline": "string",
      "deleted_date": {},
      "description": "string",
      "duration": "string",
      "is_deleted": true,
      "is_personal": true,
      "is_private": true,
      "is_role_based": true,
      "manager_email": "ava@example.com",
      "manager_id": 1,
      "modified_date": "string",
      "no": "string",
      "permissions": {},
      "project_id": 1,
      "project_name": "Ava Chen",
      "project_type": "string",
      "retainer_id": {},
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account_id` | string | Account identifier. |
| `budget_type` | string | Budget type. |
| `color` | string | Project color. |
| `company_id` | number | Related company ID. |
| `company_name` | string | Related company name. |
| `date` | string | Project start date. |
| `deadline` | string | Project deadline. |
| `deleted_date` | object | Deleted timestamp. |
| `description` | string | Project description. |
| `duration` | string | Planned duration. |
| `is_deleted` | boolean | Whether the project is deleted. |
| `is_personal` | boolean | Whether the project is personal. |
| `is_private` | boolean | Whether the project is private. |
| `is_role_based` | boolean | Whether role-based pricing is enabled. |
| `manager_email` | string | Manager email. |
| `manager_id` | number | Manager user ID. |
| `modified_date` | string | Last modified timestamp. |
| `no` | string | Project number. |
| `permissions` | object | Permissions payload. |
| `project_id` | number | Scoro project ID. |
| `project_name` | string | Project name. |
| `project_type` | string | Project type. |
| `retainer_id` | object | Related retainer ID. |
| `status` | string | Project status. |

## Native endpoint

Through the native Scoro API, this operation is `POST projects/list` (base URL `{{credentials.subdomain}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-projects.md) for the provider-specific parameters and requirements.

