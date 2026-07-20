# TLY Link Shortener: Delete Short Link

Deletes an existing short link from TLY Link Shortener.

```
DELETE https://connect.mindcloud.co/v1/universal/tLYLinkShortener/latest/actions/delete-short-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TLY Link Shortener `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/tLYLinkShortener/latest/actions/delete-short-link?connectionId=$CONNECTION_ID&shortUrl=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "shortUrl": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tLYLinkShortener/latest/actions/delete-short-link?${params}`, {
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
| `shortUrl` | string | yes | The short URL to delete. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native TLY Link Shortener API returns.

## Native endpoint

Through the native TLY Link Shortener API, this operation is `DELETE /api/v1/link` (base URL `https://api.t.ly`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-short-link.md) for the provider-specific parameters and requirements.

