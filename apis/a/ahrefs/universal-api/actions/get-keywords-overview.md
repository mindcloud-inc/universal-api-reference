# Ahrefs: Get Keywords Overview



```
GET https://connect.mindcloud.co/v1/universal/ahrefs/latest/actions/get-keywords-overview
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ahrefs `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ahrefs/latest/actions/get-keywords-overview?connectionId=$CONNECTION_ID&country=string&keywords=string&select=keyword%2Cvolume%2Cdifficulty%2Ccpc%2Ctraffic_potential" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "country": "string",
  "keywords": "string",
  "select": "keyword,volume,difficulty,cpc,traffic_potential"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ahrefs/latest/actions/get-keywords-overview?${params}`, {
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
| `country` | string | yes | Two-letter ISO 3166-1 alpha-2 country code. |
| `keywords` | string | yes | Comma-separated keywords to show metrics for. |
| `select` | string | yes | Comma-separated keyword metric columns to return. Default: `keyword,volume,difficulty,cpc,traffic_potential`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Ahrefs API returns.

## Native endpoint

Through the native Ahrefs API, this operation is `GET /keywords-explorer/overview` (base URL `https://api.ahrefs.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-keywords-overview.md) for the provider-specific parameters and requirements.

