# Short URL: Delete Short URL

Deletes an existing short URL from Short URL.

```
DELETE https://connect.mindcloud.co/v1/universal/shortURL/latest/actions/delete-short-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Short URL `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/shortURL/latest/actions/delete-short-url?connectionId=$CONNECTION_ID&baseDomain=surl.link&shortUrl=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "baseDomain": "surl.link",
  "shortUrl": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shortURL/latest/actions/delete-short-url?${params}`, {
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
| `shortUrl` | string | yes | Short URL code to delete. |

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
| `shortUrl` | string | Deleted short URL code or full short URL. |

## Native endpoint

Through the native Short URL API, this operation is `GET https://:baseDomain/api/wrapper_api.php` (base URL `https://surl.link`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-short-url.md) for the provider-specific parameters and requirements.

