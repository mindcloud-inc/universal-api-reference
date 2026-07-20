# ClustDoc: List Portals



```
GET https://connect.mindcloud.co/v1/universal/clustDoc/latest/actions/list-portals
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClustDoc `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clustDoc/latest/actions/list-portals?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clustDoc/latest/actions/list-portals?${params}`, {
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
      "created_at": "string",
      "id": 1,
      "iframe_code": "string",
      "is_live": true,
      "owner_id": 1,
      "public_url": "https://example.com",
      "team_id": 1,
      "templates_ids": [
        1
      ],
      "title": "string",
      "updated_at": "string",
      "vanity_slug": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | string |  |
| `id` | number |  |
| `iframe_code` | string |  |
| `is_live` | boolean |  |
| `owner_id` | number |  |
| `public_url` | string |  |
| `team_id` | number |  |
| `templates_ids` | array<number> |  |
| `title` | string |  |
| `updated_at` | string |  |
| `vanity_slug` | string |  |

## Native endpoint

Through the native ClustDoc API, this operation is `GET /portals` (base URL `https://api.clustdoc.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-portals.md) for the provider-specific parameters and requirements.

