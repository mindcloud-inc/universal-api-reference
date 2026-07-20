# Scoro: View Project

Retrieves project details from Scoro.

```
GET https://connect.mindcloud.co/v1/universal/scoro/latest/actions/view-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scoro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scoro/latest/actions/view-project?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scoro/latest/actions/view-project?${params}`, {
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
| `id` | string | no | Scoro project ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "account_id": "string",
      "budget_type": "string",
      "company_id": 1,
      "company_name": "Ava Chen",
      "date": "string",
      "deadline": "string",
      "deleted_date": {},
      "description": "string",
      "duration": "string",
      "is_deleted": true,
      "is_role_based": true,
      "local_price_list_id": 1,
      "manager_email": "ava@example.com",
      "manager_id": 1,
      "modified_date": "string",
      "no": "string",
      "phases": [
        {}
      ],
      "project_accounts": [
        "string"
      ],
      "project_id": 1,
      "project_name": "Ava Chen",
      "project_type": "string",
      "project_users": [
        {}
      ],
      "retainer_id": {},
      "status": "string",
      "status_name": "Ava Chen",
      "tags": [
        "string"
      ]
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
| `company_id` | number | Related company ID. |
| `company_name` | string | Related company name. |
| `date` | string | Project start date. |
| `deadline` | string | Project deadline. |
| `deleted_date` | object | Deleted timestamp. |
| `description` | string | Project description. |
| `duration` | string | Planned duration. |
| `is_deleted` | boolean | Whether the project is deleted. |
| `is_role_based` | boolean | Whether role-based pricing is enabled. |
| `local_price_list_id` | number | Local price list ID. |
| `manager_email` | string | Manager email. |
| `manager_id` | number | Manager user ID. |
| `modified_date` | string | Last modified timestamp. |
| `no` | string | Project number. |
| `phases` | array<object> | Project phases. |
| `project_accounts` | array<string> | Linked project accounts. |
| `project_id` | number | Scoro project ID. |
| `project_name` | string | Project name. |
| `project_type` | string | Project type. |
| `project_users` | array<object> | Assigned project users. |
| `retainer_id` | object | Related retainer ID. |
| `status` | string | Project status. |
| `status_name` | string | Project status label. |
| `tags` | array<string> | Project tags. |

## Native endpoint

Through the native Scoro API, this operation is `POST projects/view/:id` (base URL `{{credentials.subdomain}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/view-project.md) for the provider-specific parameters and requirements.

