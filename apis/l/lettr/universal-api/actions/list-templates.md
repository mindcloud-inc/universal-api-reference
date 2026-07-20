# Lettr: List Templates



```
GET https://connect.mindcloud.co/v1/universal/lettr/latest/actions/list-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lettr `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lettr/latest/actions/list-templates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lettr/latest/actions/list-templates?${params}`, {
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
        "pagination": {
          "current_page": 1,
          "last_page": 1,
          "per_page": 1,
          "total": 1
        },
        "templates": {
          "created_at": "2026-05-07T12:00:00.000Z",
          "folder_id": 1,
          "id": 1,
          "name": "Ava Chen",
          "project_id": 1,
          "slug": "string",
          "updated_at": "2026-05-07T12:00:00.000Z"
        }
      },
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Template list payload. |
| `data.pagination` | object | Pagination details. |
| `data.pagination.current_page` | number | Current page number. |
| `data.pagination.last_page` | number | Last available page number. |
| `data.pagination.per_page` | number | Items per page. |
| `data.pagination.total` | number | Total template count. |
| `data.templates` | array<object> | Templates in the selected project scope. |
| `data.templates.created_at` | date | Creation timestamp. |
| `data.templates.folder_id` | number | Owning folder ID. |
| `data.templates.id` | number | Template ID. |
| `data.templates.name` | string | Template name. |
| `data.templates.project_id` | number | Owning project ID. |
| `data.templates.slug` | string | Template slug. |
| `data.templates.updated_at` | date | Last update timestamp. |
| `message` | string | Template list status message. |

## Native endpoint

Through the native Lettr API, this operation is `GET /templates` (base URL `https://app.lettr.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-templates.md) for the provider-specific parameters and requirements.

