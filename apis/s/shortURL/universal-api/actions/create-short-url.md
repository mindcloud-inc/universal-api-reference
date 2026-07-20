# Short URL: Create Short URL

Creates a new short URL in Short URL.

```
POST https://connect.mindcloud.co/v1/universal/shortURL/latest/actions/create-short-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Short URL `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/shortURL/latest/actions/create-short-url" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "baseDomain": "surl.link",
  "longUrl": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/shortURL/latest/actions/create-short-url', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "baseDomain": "surl.link",
    "longUrl": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `baseDomain` | string | yes | Short URL domain to use for this request. One of: `0`, `1`, `2`, `3`. Default: `surl.link`. |
| `longUrl` | string | yes | Destination URL to redirect to. |
| `shortUrl` | string | no | Optional custom short URL code. |
| `description` | string | no | Optional short URL description. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `createdBy` | string | no | Optional creator identifier. |
| `expiryDate` | date | no | Optional expiration date in YYYY-MM-DD format. |
| `password` | string | no | Optional access password. |
| `maxUses` | number | no | Optional maximum number of uses. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": "string",
      "response": "string",
      "responseCode": "string",
      "shortUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | string | Additional provider data. |
| `response` | string | Provider response message. |
| `responseCode` | string | Provider response code. |
| `shortUrl` | string | Created short URL code or full short URL. |

## Native endpoint

Through the native Short URL API, this operation is `GET https://:baseDomain/api/wrapper_api.php` (base URL `https://surl.link`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-short-url.md) for the provider-specific parameters and requirements.

