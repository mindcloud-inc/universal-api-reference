# GitScrum: List Projects

Retrieves a list of GitScrum projects.

```
GET https://connect.mindcloud.co/v1/universal/gitScrum/latest/actions/list-projects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GitScrum `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gitScrum/latest/actions/list-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gitScrum/latest/actions/list-projects?${params}`, {
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
| `companySlug` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "background": "string",
      "background_thumb": "string",
      "budget": 1,
      "budget_used": 1,
      "category_id": 1,
      "code": "string",
      "company": {},
      "contact_company": {},
      "contact_company_id": 1,
      "created_at": {},
      "dates": {},
      "id": 1,
      "labels": [
        {}
      ],
      "logo": "string",
      "name": "Ava Chen",
      "owner": {},
      "percent": 1,
      "proposal": {},
      "pure_name": "Ava Chen",
      "recurring": true,
      "slug": "string",
      "stats": {},
      "status": {},
      "users": [
        {}
      ],
      "uuid": "string",
      "visibility": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `background` | string |  |
| `background_thumb` | string |  |
| `budget` | number |  |
| `budget_used` | number |  |
| `category_id` | number |  |
| `code` | string |  |
| `company` | object |  |
| `contact_company` | object |  |
| `contact_company_id` | number |  |
| `created_at` | object |  |
| `dates` | object |  |
| `id` | number |  |
| `labels` | array<object> |  |
| `logo` | string |  |
| `name` | string |  |
| `owner` | object |  |
| `percent` | number |  |
| `proposal` | object |  |
| `pure_name` | string |  |
| `recurring` | boolean |  |
| `slug` | string |  |
| `stats` | object |  |
| `status` | object |  |
| `users` | array<object> |  |
| `uuid` | string |  |
| `visibility` | object |  |

## Native endpoint

Through the native GitScrum API, this operation is `GET /projects` (base URL `https://services.gitscrum.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-projects.md) for the provider-specific parameters and requirements.

