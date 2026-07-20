# Ahrefs: List Backlinks



```
GET https://connect.mindcloud.co/v1/universal/ahrefs/latest/actions/list-backlinks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ahrefs `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ahrefs/latest/actions/list-backlinks?connectionId=$CONNECTION_ID&target=string&select=url_from%2Curl_to%2Canchor%2Cdomain_rating_source%2Cfirst_seen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "target": "string",
  "select": "url_from,url_to,anchor,domain_rating_source,first_seen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ahrefs/latest/actions/list-backlinks?${params}`, {
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
| `mode` | string | no | Target scope: exact, prefix, domain, or subdomains. |
| `target` | string | yes | Domain or URL to analyze. |
| `select` | string | yes | Comma-separated backlink columns to return. Default: `url_from,url_to,anchor,domain_rating_source,first_seen`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Ahrefs API returns.

## Native endpoint

Through the native Ahrefs API, this operation is `GET /site-explorer/all-backlinks` (base URL `https://api.ahrefs.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-backlinks.md) for the provider-specific parameters and requirements.

