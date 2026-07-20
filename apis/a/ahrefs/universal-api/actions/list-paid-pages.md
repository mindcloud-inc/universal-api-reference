# Ahrefs: List Paid Pages



```
GET https://connect.mindcloud.co/v1/universal/ahrefs/latest/actions/list-paid-pages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ahrefs `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ahrefs/latest/actions/list-paid-pages?connectionId=$CONNECTION_ID&target=string&date=2026-05-07T12%3A00%3A00.000Z&select=url%2Csum_traffic%2Ckeywords%2Cvalue" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "target": "string",
  "date": "2026-05-07T12:00:00.000Z",
  "select": "url,sum_traffic,keywords,value"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ahrefs/latest/actions/list-paid-pages?${params}`, {
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
| `date` | date | yes | Report date in YYYY-MM-DD format. |
| `select` | string | yes | Comma-separated paid-page columns to return. Default: `url,sum_traffic,keywords,value`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Ahrefs API returns.

## Native endpoint

Through the native Ahrefs API, this operation is `GET /site-explorer/paid-pages` (base URL `https://api.ahrefs.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-paid-pages.md) for the provider-specific parameters and requirements.

