# Ahrefs: List Organic Keywords



```
GET https://connect.mindcloud.co/v1/universal/ahrefs/latest/actions/list-organic-keywords
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ahrefs `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ahrefs/latest/actions/list-organic-keywords?connectionId=$CONNECTION_ID&target=string&date=2026-05-07T12%3A00%3A00.000Z&select=keyword%2Cbest_position%2Cvolume%2Csum_traffic%2Ckeyword_difficulty" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "target": "string",
  "date": "2026-05-07T12:00:00.000Z",
  "select": "keyword,best_position,volume,sum_traffic,keyword_difficulty"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ahrefs/latest/actions/list-organic-keywords?${params}`, {
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
| `select` | string | yes | Comma-separated organic keyword columns to return. Default: `keyword,best_position,volume,sum_traffic,keyword_difficulty`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Ahrefs API returns.

## Native endpoint

Through the native Ahrefs API, this operation is `GET /site-explorer/organic-keywords` (base URL `https://api.ahrefs.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-organic-keywords.md) for the provider-specific parameters and requirements.

