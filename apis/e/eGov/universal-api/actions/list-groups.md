# e-Gov: List Groups

Retrieves groups from e-Gov.

```
GET https://connect.mindcloud.co/v1/universal/eGov/latest/actions/list-groups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a e-Gov `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eGov/latest/actions/list-groups?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eGov/latest/actions/list-groups?${params}`, {
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
| `all_fields` | boolean | no | Return full group records instead of names. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `include_dataset_count` | boolean | no |  |
| `include_extras` | boolean | no |  |
| `include_tags` | boolean | no |  |
| `include_groups` | boolean | no |  |
| `include_users` | boolean | no |  |
| `sort` | string | no |  |
| `order_by` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "approval_status": "string",
      "created": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "display_name": "Ava Chen",
      "id": "string",
      "image_display_url": "https://example.com",
      "image_url": "https://example.com",
      "is_organization": true,
      "name": "Ava Chen",
      "num_followers": 1,
      "package_count": 1,
      "state": "string",
      "title": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `approval_status` | string |  |
| `created` | date |  |
| `description` | string |  |
| `display_name` | string |  |
| `id` | string |  |
| `image_display_url` | string |  |
| `image_url` | string |  |
| `is_organization` | boolean |  |
| `name` | string |  |
| `num_followers` | number |  |
| `package_count` | number |  |
| `state` | string |  |
| `title` | string |  |
| `type` | string |  |

## Native endpoint

Through the native e-Gov API, this operation is `GET /group_list` (base URL `https://data.e-gov.go.jp/data/api/action`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-groups.md) for the provider-specific parameters and requirements.

