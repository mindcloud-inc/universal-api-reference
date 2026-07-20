# GitScrum: List Workflows

Retrieves a list of GitScrum workflows.

```
GET https://connect.mindcloud.co/v1/universal/gitScrum/latest/actions/list-workflows
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GitScrum `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gitScrum/latest/actions/list-workflows?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gitScrum/latest/actions/list-workflows?${params}`, {
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
| `projectSlug` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "autoarchive": 1,
      "clear_old_labels": true,
      "clear_old_users": true,
      "color": "string",
      "default": true,
      "description": "string",
      "emails": [
        "ava@example.com"
      ],
      "id": 1,
      "labels": [
        {}
      ],
      "position": 1,
      "slug": "string",
      "state": 1,
      "status": {},
      "tasks": {},
      "title": "string",
      "users": [
        {}
      ],
      "value_fixed": 1,
      "wip": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `autoarchive` | number |  |
| `clear_old_labels` | boolean |  |
| `clear_old_users` | boolean |  |
| `color` | string |  |
| `default` | boolean |  |
| `description` | string |  |
| `emails` | array<string> |  |
| `id` | number |  |
| `labels` | array<object> |  |
| `position` | number |  |
| `slug` | string |  |
| `state` | number |  |
| `status` | object |  |
| `tasks` | object |  |
| `title` | string |  |
| `users` | array<object> |  |
| `value_fixed` | number |  |
| `wip` | number |  |

## Native endpoint

Through the native GitScrum API, this operation is `GET /projects-workflows` (base URL `https://services.gitscrum.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-workflows.md) for the provider-specific parameters and requirements.

