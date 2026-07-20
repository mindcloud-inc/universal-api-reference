# Short URL: List Short URLs

Retrieves short URLs from Short URL.

```
GET https://connect.mindcloud.co/v1/universal/shortURL/latest/actions/list-short-urls
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Short URL `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shortURL/latest/actions/list-short-urls?connectionId=$CONNECTION_ID&baseDomain=surl.link" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "baseDomain": "surl.link"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shortURL/latest/actions/list-short-urls?${params}`, {
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
| `baseDomain` | string | yes | Short URL domain to use for this request. One of: `0`, `1`, `2`, `3`. Default: `surl.link`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `createdBy` | string | no | Optional creator filter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdBy": "string",
      "createdDate": "string",
      "description": "string",
      "expiryDate": "string",
      "hasPassword": "string",
      "lastAccessed": "string",
      "longUrl": "https://example.com",
      "shortUrl": "https://example.com",
      "status": "string",
      "totalUses": "string",
      "totalVisits": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdBy` | string | Creator identifier. |
| `createdDate` | string | Created date. |
| `description` | string | Short URL description. |
| `expiryDate` | string | Expiration date. |
| `hasPassword` | string | Password protection status. |
| `lastAccessed` | string | Last access timestamp. |
| `longUrl` | string | Destination URL. |
| `shortUrl` | string | Short URL code or full short URL. |
| `status` | string | Short URL status. |
| `totalUses` | string | Maximum or total allowed uses. |
| `totalVisits` | string | Total visits. |

## Native endpoint

Through the native Short URL API, this operation is `GET https://:baseDomain/api/wrapper_api.php` (base URL `https://surl.link`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-short-urls.md) for the provider-specific parameters and requirements.

