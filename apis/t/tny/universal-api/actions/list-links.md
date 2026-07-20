# Tny: List Links

Retrieves short links from Tny.

```
GET https://connect.mindcloud.co/v1/universal/tny/latest/actions/list-links
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tny `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tny/latest/actions/list-links?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tny/latest/actions/list-links?${params}`, {
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
| `scope` | list | no | Return links for the current API key only or for all API keys on the account. One of: `all`, `key`. Default: `key`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "clickCount": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "customDomain": "string",
      "id": "string",
      "longUrl": "https://example.com",
      "shortUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `clickCount` | number | Tracked click count for the link. |
| `createdAt` | date | When the short link was created. |
| `customDomain` | string | Custom domain used by the link when present. |
| `id` | string | Short link slug identifier. |
| `longUrl` | string | Original destination URL. |
| `shortUrl` | string | Shortened URL. |

## Native endpoint

Through the native Tny API, this operation is `GET /api/v1/links` (base URL `https://www.tny.dev`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-links.md) for the provider-specific parameters and requirements.

