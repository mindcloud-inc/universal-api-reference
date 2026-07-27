# Google Search Console: Delete Site



```
DELETE https://connect.mindcloud.co/v1/universal/googleSearchConsole/latest/actions/delete-site
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Search Console `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/googleSearchConsole/latest/actions/delete-site?connectionId=$CONNECTION_ID&siteUrl=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "siteUrl": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleSearchConsole/latest/actions/delete-site?${params}`, {
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
| `siteUrl` | list<string> | yes | The Search Console property URL to remove, such as a URL-prefix property or a sc-domain property. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Google Search Console API returns.

## Native endpoint

Through the native Google Search Console API, this operation is `DELETE sites/:siteUrl` (base URL `https://www.googleapis.com/webmasters/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-site.md) for the provider-specific parameters and requirements.

