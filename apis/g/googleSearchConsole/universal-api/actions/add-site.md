# Google Search Console: Add Site



```
POST https://connect.mindcloud.co/v1/universal/googleSearchConsole/latest/actions/add-site
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Search Console `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/googleSearchConsole/latest/actions/add-site" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "siteUrl": "sc-domain:example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/googleSearchConsole/latest/actions/add-site', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "siteUrl": "sc-domain:example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `siteUrl` | string | yes | The Search Console property URL to add, such as a URL-prefix property or a sc-domain property. Example: `sc-domain:example.com`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Google Search Console API returns.

## Native endpoint

Through the native Google Search Console API, this operation is `PUT sites/:siteUrl` (base URL `https://www.googleapis.com/webmasters/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-site.md) for the provider-specific parameters and requirements.

