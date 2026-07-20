# Invision Community: List CMS Categories



```
GET https://connect.mindcloud.co/v1/universal/invisionCommunity/latest/actions/list-cms-categories
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Invision Community `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/invisionCommunity/latest/actions/list-cms-categories?connectionId=$CONNECTION_ID&limit=25&offset=0&database_id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "database_id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/invisionCommunity/latest/actions/list-cms-categories?${params}`, {
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
| `database_id` | number | yes | Database identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "class": "string",
      "club": 1,
      "id": 1,
      "name": "Ava Chen",
      "page": 1,
      "parentId": 1,
      "perPage": 1,
      "results": [
        {}
      ],
      "totalPages": 1,
      "totalResults": 1,
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `class` | string |  |
| `club` | number |  |
| `id` | number |  |
| `name` | string |  |
| `page` | number |  |
| `parentId` | number |  |
| `perPage` | number |  |
| `results` | array<object> |  |
| `totalPages` | number |  |
| `totalResults` | number |  |
| `url` | string |  |

## Native endpoint

Through the native Invision Community API, this operation is `GET /cms/categories/:database_id` (base URL `{{credentials.communityBaseUrl}}/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-cms-categories.md) for the provider-specific parameters and requirements.

