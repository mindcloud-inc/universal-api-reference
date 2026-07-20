# updown.io: List Status Pages

Retrieves all status pages from updown.io.

```
GET https://connect.mindcloud.co/v1/universal/updownio/latest/actions/list-status-pages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a updown.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/updownio/latest/actions/list-status-pages?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/updownio/latest/actions/list-status-pages?${params}`, {
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
      "access_key": "string",
      "checks": [
        "string"
      ],
      "description": "string",
      "name": "Ava Chen",
      "token": "string",
      "url": "https://example.com",
      "visibility": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `access_key` | string | Protected-page access key. |
| `checks` | array<string> | Check tokens shown on the page. |
| `description` | string | Status page description. |
| `name` | string | Status page name. |
| `token` | string | Status page token. |
| `url` | string | Public status page URL. |
| `visibility` | string | Status page visibility. |

## Native endpoint

Through the native updown.io API, this operation is `GET /status_pages` (base URL `https://updown.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-status-pages.md) for the provider-specific parameters and requirements.

