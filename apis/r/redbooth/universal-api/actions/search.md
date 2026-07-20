# Redbooth: Search

Finds matching records in your Redbooth account.

```
GET https://connect.mindcloud.co/v1/universal/redbooth/latest/actions/search
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Redbooth `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/redbooth/latest/actions/search?connectionId=$CONNECTION_ID&term=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "term": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/redbooth/latest/actions/search?${params}`, {
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
| `term` | string | yes | Search term |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": 1,
      "icon": "string",
      "parent_id": 1,
      "parent_type": "string",
      "tag_ids": [
        1
      ],
      "target_id": 1,
      "target_type": "string",
      "title": "string",
      "updated_at": 1,
      "user_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | number |  |
| `icon` | string |  |
| `parent_id` | number |  |
| `parent_type` | string |  |
| `tag_ids` | array<number> |  |
| `target_id` | number |  |
| `target_type` | string |  |
| `title` | string |  |
| `updated_at` | number |  |
| `user_id` | number |  |

## Native endpoint

Through the native Redbooth API, this operation is `GET /search` (base URL `https://redbooth.com/api/3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search.md) for the provider-specific parameters and requirements.

