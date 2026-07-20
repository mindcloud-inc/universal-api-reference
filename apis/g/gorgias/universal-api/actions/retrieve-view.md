# Gorgias: Retrieve View

Retrieves a view from Gorgias.

```
GET https://connect.mindcloud.co/v1/universal/gorgias/latest/actions/retrieve-view
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gorgias `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gorgias/latest/actions/retrieve-view?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gorgias/latest/actions/retrieve-view?${params}`, {
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
| `id` | string | yes | View ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "category": "string",
      "created_datetime": "string",
      "deactivated_datetime": "string",
      "decoration": {},
      "fields": [
        {}
      ],
      "filters": [
        {}
      ],
      "filters_ast": {},
      "id": 1,
      "name": "Ava Chen",
      "order_by": "string",
      "order_dir": "string",
      "search": "string",
      "section_id": 1,
      "shared_with_teams": [
        {}
      ],
      "shared_with_users": [
        {}
      ],
      "slug": "string",
      "type": "string",
      "uri": "string",
      "visibility": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `category` | string |  |
| `created_datetime` | string |  |
| `deactivated_datetime` | string |  |
| `decoration` | object |  |
| `fields` | array<object> |  |
| `filters` | array<object> |  |
| `filters_ast` | object |  |
| `id` | number |  |
| `name` | string |  |
| `order_by` | string |  |
| `order_dir` | string |  |
| `search` | string |  |
| `section_id` | number |  |
| `shared_with_teams` | array<object> |  |
| `shared_with_users` | array<object> |  |
| `slug` | string |  |
| `type` | string |  |
| `uri` | string |  |
| `visibility` | string |  |

## Native endpoint

Through the native Gorgias API, this operation is `GET /views/:id` (base URL `https://{{credentials.subdomain}}.gorgias.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-view.md) for the provider-specific parameters and requirements.

