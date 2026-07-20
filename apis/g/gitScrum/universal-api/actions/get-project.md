# GitScrum: Get Project

Retrieves details for a specific GitScrum project.

```
GET https://connect.mindcloud.co/v1/universal/gitScrum/latest/actions/get-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GitScrum `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gitScrum/latest/actions/get-project?connectionId=$CONNECTION_ID&companySlug=string&slug=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "companySlug": "string",
  "slug": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gitScrum/latest/actions/get-project?${params}`, {
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
| `companySlug` | string | yes |  |
| `slug` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "api_task": {},
      "background": "string",
      "background_thumb": "string",
      "boards": [
        {}
      ],
      "budget": {},
      "category_id": 1,
      "closed_tasks": [
        1
      ],
      "code": "string",
      "company": {},
      "created_at": {},
      "dates": {},
      "description": "string",
      "hourly_rate": 1,
      "id": 1,
      "integration": {},
      "labels": [
        {}
      ],
      "logged_user_role": {},
      "logo": "string",
      "my_contribution": 1,
      "name": "Ava Chen",
      "owner": {},
      "percent": 1,
      "permissions": {},
      "recurring": true,
      "settings": {},
      "sidebar": [
        {}
      ],
      "slug": "string",
      "stats": {},
      "status": {},
      "users": [
        {}
      ],
      "uuid": "string",
      "visibility": {},
      "workspaceDataHistory": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `api_task` | object |  |
| `background` | string |  |
| `background_thumb` | string |  |
| `boards` | array<object> |  |
| `budget` | object |  |
| `category_id` | number |  |
| `closed_tasks` | array<number> |  |
| `code` | string |  |
| `company` | object |  |
| `created_at` | object |  |
| `dates` | object |  |
| `description` | string |  |
| `hourly_rate` | number |  |
| `id` | number |  |
| `integration` | object |  |
| `labels` | array<object> |  |
| `logged_user_role` | object |  |
| `logo` | string |  |
| `my_contribution` | number |  |
| `name` | string |  |
| `owner` | object |  |
| `percent` | number |  |
| `permissions` | object |  |
| `recurring` | boolean |  |
| `settings` | object |  |
| `sidebar` | array<object> |  |
| `slug` | string |  |
| `stats` | object |  |
| `status` | object |  |
| `users` | array<object> |  |
| `uuid` | string |  |
| `visibility` | object |  |
| `workspaceDataHistory` | object |  |

## Native endpoint

Through the native GitScrum API, this operation is `GET /projects/:slug` (base URL `https://services.gitscrum.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project.md) for the provider-specific parameters and requirements.

