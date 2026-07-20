# Ahrefs: Run Batch Analysis



```
GET https://connect.mindcloud.co/v1/universal/ahrefs/latest/actions/run-batch-analysis
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ahrefs `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ahrefs/latest/actions/run-batch-analysis?connectionId=$CONNECTION_ID&select%5B%5D=domain_rating%2Cbacklinks%2Crefdomains%2Corg_traffic&targets%5B%5D=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "select[]": "domain_rating,backlinks,refdomains,org_traffic",
  "targets[]": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ahrefs/latest/actions/run-batch-analysis?${params}`, {
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
| `select[]` | array<string> | yes | Fields to include in the batch analysis response. Example: `domain_rating,backlinks,refdomains,org_traffic`. |
| `targets[]` | array<object> | yes | Targets to analyze. Each target includes a URL plus mode and protocol. Example: `[object Object]`. |
| `country` | string | no | Two-letter ISO 3166-1 alpha-2 country code. |
| `volumeMode` | string | no | Search volume calculation mode: monthly or average. Default: `monthly`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Ahrefs API returns.

## Native endpoint

Through the native Ahrefs API, this operation is `POST /batch-analysis/batch-analysis` (base URL `https://api.ahrefs.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/run-batch-analysis.md) for the provider-specific parameters and requirements.

