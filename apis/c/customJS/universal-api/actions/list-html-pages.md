# CustomJS: List HTML Pages

Retrieves hosted HTML pages from CustomJS.

```
GET https://connect.mindcloud.co/v1/universal/customJS/latest/actions/list-html-pages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CustomJS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/customJS/latest/actions/list-html-pages?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/customJS/latest/actions/list-html-pages?${params}`, {
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
      "cname": "Ava Chen",
      "created_at": "2026-05-07T12:00:00.000Z",
      "defaults": [
        {
          "path": "string",
          "type": "string",
          "values": {
            "layout": "string",
            "permalink": "https://example.com"
          }
        }
      ],
      "domain": "string",
      "id": "string",
      "metadata": {
        "permalink": "https://example.com"
      },
      "timezone": "string",
      "title": "string",
      "updated_at": "2026-05-07T12:00:00.000Z",
      "user_id": "string",
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cname` | string |  |
| `created_at` | date |  |
| `defaults[].path` | string |  |
| `defaults[].type` | string |  |
| `defaults[].values.layout` | string |  |
| `defaults[].values.permalink` | string |  |
| `domain` | string |  |
| `id` | string |  |
| `metadata.permalink` | string |  |
| `timezone` | string |  |
| `title` | string |  |
| `updated_at` | date |  |
| `user_id` | string |  |
| `version` | string |  |

## Native endpoint

Through the native CustomJS API, this operation is `GET https://api.app.customjs.io/pages/api/page` (base URL `https://e.customjs.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-html-pages.md) for the provider-specific parameters and requirements.

