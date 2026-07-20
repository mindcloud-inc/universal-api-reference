# Ahrefs: List Linked Domains



```
GET https://connect.mindcloud.co/v1/universal/ahrefs/latest/actions/list-linked-domains
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ahrefs `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ahrefs/latest/actions/list-linked-domains?connectionId=$CONNECTION_ID&target=string&select=domain%2Clinks_external%2Cfirst_seen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "target": "string",
  "select": "domain,links_external,first_seen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ahrefs/latest/actions/list-linked-domains?${params}`, {
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
| `target` | string | yes | Domain or URL to analyze. |
| `select` | string | yes | Comma-separated linked-domain columns to return. Default: `domain,links_external,first_seen`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Ahrefs API returns.

## Native endpoint

Through the native Ahrefs API, this operation is `GET /site-explorer/linkeddomains` (base URL `https://api.ahrefs.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-linked-domains.md) for the provider-specific parameters and requirements.

