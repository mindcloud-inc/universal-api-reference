# e-Gov: Get Group

Retrieves a group from e-Gov.

```
GET https://connect.mindcloud.co/v1/universal/eGov/latest/actions/get-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a e-Gov `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eGov/latest/actions/get-group?connectionId=$CONNECTION_ID&id=gr_0200" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "gr_0200"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eGov/latest/actions/get-group?${params}`, {
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
| `id` | string | yes | Default: `gr_0200`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `include_dataset_count` | boolean | no |  |
| `include_tags` | boolean | no |  |
| `include_groups` | boolean | no |  |
| `include_users` | boolean | no |  |

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
      "extras": [
        {}
      ],
      "groups": [
        "string"
      ],
      "id": "string",
      "image_display_url": "https://example.com",
      "image_url": "https://example.com",
      "is_organization": true,
      "name": "Ava Chen",
      "num_followers": 1,
      "package_count": 1,
      "state": "string",
      "tags": [
        "string"
      ],
      "title": "string",
      "type": "string",
      "users": [
        {}
      ]
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
| `extras` | array<object> |  |
| `groups` | array<string> |  |
| `id` | string |  |
| `image_display_url` | string |  |
| `image_url` | string |  |
| `is_organization` | boolean |  |
| `name` | string |  |
| `num_followers` | number |  |
| `package_count` | number |  |
| `state` | string |  |
| `tags` | array<string> |  |
| `title` | string |  |
| `type` | string |  |
| `users` | array<object> |  |

## Native endpoint

Through the native e-Gov API, this operation is `GET /group_show` (base URL `https://data.e-gov.go.jp/data/api/action`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-group.md) for the provider-specific parameters and requirements.

