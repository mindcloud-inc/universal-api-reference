# Ahrefs: Get SERP Overview



```
GET https://connect.mindcloud.co/v1/universal/ahrefs/latest/actions/get-serp-overview
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ahrefs `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ahrefs/latest/actions/get-serp-overview?connectionId=$CONNECTION_ID&keyword=string&country=string&select=position%2Curl%2Ctitle%2Cdomain_rating%2Ctraffic" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "keyword": "string",
  "country": "string",
  "select": "position,url,title,domain_rating,traffic"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ahrefs/latest/actions/get-serp-overview?${params}`, {
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
| `keyword` | string | yes | Keyword to return SERP overview for. |
| `topPositions` | string | no | Number of top organic SERP positions to return. |
| `country` | string | yes | Two-letter ISO 3166-1 alpha-2 country code. |
| `select` | string | yes | Comma-separated SERP columns to return. Default: `position,url,title,domain_rating,traffic`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "positions": {
        "domain_rating": 1,
        "position": 1,
        "refdomains": 1,
        "title": "string",
        "traffic": 1,
        "update_date": "2026-05-07T12:00:00.000Z",
        "url": "https://example.com"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `positions` | array<object> | SERP positions returned by Ahrefs. |
| `positions.domain_rating` | number |  |
| `positions.position` | number |  |
| `positions.refdomains` | number |  |
| `positions.title` | string |  |
| `positions.traffic` | number |  |
| `positions.update_date` | date |  |
| `positions.url` | string |  |

## Native endpoint

Through the native Ahrefs API, this operation is `GET /serp-overview/serp-overview` (base URL `https://api.ahrefs.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-serp-overview.md) for the provider-specific parameters and requirements.

