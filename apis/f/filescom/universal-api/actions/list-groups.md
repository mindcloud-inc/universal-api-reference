# Files.com: List Groups

Retrieves group records from a Files.com site.

```
GET https://connect.mindcloud.co/v1/universal/filescom/latest/actions/list-groups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Files.com `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/filescom/latest/actions/list-groups?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/filescom/latest/actions/list-groups?${params}`, {
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
| `includeParentSiteGroups` | boolean | no | Include groups inherited from the parent site. |
| `perPage` | number | no | Maximum number of items to return in one page. |
| `cursor` | string | no | Cursor token returned by a previous page. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "admin_ids": [
        1
      ],
      "created_at": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "name": "Ava Chen",
      "notes": "string",
      "user_ids": [
        1
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `admin_ids` | array<number> |  |
| `created_at` | date |  |
| `id` | number |  |
| `name` | string |  |
| `notes` | string |  |
| `user_ids` | array<number> |  |

## Native endpoint

Through the native Files.com API, this operation is `GET /groups` (base URL `{{credentials.siteUrl}}/api/rest/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-groups.md) for the provider-specific parameters and requirements.

