# Recut URL Shortener: List Links

Retrieves links from Recut URL Shortener.

```
GET https://connect.mindcloud.co/v1/universal/recutURLShortener/latest/actions/list-links
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Recut URL Shortener `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/recutURLShortener/latest/actions/list-links?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/recutURLShortener/latest/actions/list-links?${params}`, {
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
| `order` | string | no | Sort links by `date` or `click`. Example: `date`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `short` | string | no | Search using the short URL. When provided, the docs say other parameters are ignored. |
| `q` | string | no | Search links using a keyword. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "alias": "string",
      "campaign": 1,
      "channel": [
        1
      ],
      "clicks": 1,
      "date": "string",
      "description": "string",
      "domain": "string",
      "id": 1,
      "longurl": "https://example.com",
      "shorturl": "https://example.com",
      "title": "string",
      "uniqueclicks": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `alias` | string | Short link alias. |
| `campaign` | number | Attached campaign ID. |
| `channel` | array<number> | Attached channel IDs. |
| `clicks` | number | Total clicks. |
| `date` | string | Creation timestamp. |
| `description` | string | Link description. |
| `domain` | string | Short domain. |
| `id` | number | Link ID. |
| `longurl` | string | Destination URL. |
| `shorturl` | string | Short URL. |
| `title` | string | Resolved page title. |
| `uniqueclicks` | number | Unique clicks. |

## Native endpoint

Through the native Recut URL Shortener API, this operation is `GET /urls` (base URL `https://app.recut.in/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-links.md) for the provider-specific parameters and requirements.

