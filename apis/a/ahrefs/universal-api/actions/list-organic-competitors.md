# Ahrefs: List Organic Competitors



```
GET https://connect.mindcloud.co/v1/universal/ahrefs/latest/actions/list-organic-competitors
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ahrefs `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ahrefs/latest/actions/list-organic-competitors?connectionId=$CONNECTION_ID&target=string&date=2026-05-07T12%3A00%3A00.000Z&country=string&select=competitor_domain%2Cdomain_rating%2Ckeywords_common%2Ctraffic%2Cvalue" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "target": "string",
  "date": "2026-05-07T12:00:00.000Z",
  "country": "string",
  "select": "competitor_domain,domain_rating,keywords_common,traffic,value"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ahrefs/latest/actions/list-organic-competitors?${params}`, {
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
| `country` | string | yes | Two-letter ISO 3166-1 alpha-2 country code. |
| `select` | string | yes | Comma-separated competitor columns to return. Default: `competitor_domain,domain_rating,keywords_common,traffic,value`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Ahrefs API returns.

## Native endpoint

Through the native Ahrefs API, this operation is `GET /site-explorer/organic-competitors` (base URL `https://api.ahrefs.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-organic-competitors.md) for the provider-specific parameters and requirements.

