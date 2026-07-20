# Papyrs: List Pages



```
GET https://connect.mindcloud.co/v1/universal/papyrs/latest/actions/list-pages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Papyrs `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/papyrs/latest/actions/list-pages?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/papyrs/latest/actions/list-pages?${params}`, {
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
      "category": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "created_by": "string",
      "id": "string",
      "is_public": 1,
      "slug": "string",
      "tags": [
        "string"
      ],
      "title": "string",
      "updated_at": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `category` | string | Page category path. |
| `created_at` | date | Page creation timestamp. |
| `created_by` | string | Page creator display name. |
| `id` | string | Papyrs page ID. |
| `is_public` | number | Whether the page is public. |
| `slug` | string | Page slug. |
| `tags` | array<string> | Page tags. |
| `title` | string | Page title. |
| `updated_at` | date | Page update timestamp. |
| `url` | string | Absolute page URL. |

## Native endpoint

Through the native Papyrs API, this operation is `GET /pages/all/` (base URL `https://{{credentials.subdomain}}.papyrs.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-pages.md) for the provider-specific parameters and requirements.

