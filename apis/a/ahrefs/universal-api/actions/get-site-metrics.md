# Ahrefs: Get Site Metrics



```
GET https://connect.mindcloud.co/v1/universal/ahrefs/latest/actions/get-site-metrics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ahrefs `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ahrefs/latest/actions/get-site-metrics?connectionId=$CONNECTION_ID&target=string&date=2026-05-07T12%3A00%3A00.000Z" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "target": "string",
  "date": "2026-05-07T12:00:00.000Z"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ahrefs/latest/actions/get-site-metrics?${params}`, {
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
| `country` | string | no | Two-letter ISO 3166-1 alpha-2 country code. |
| `target` | string | yes | Domain or URL to analyze. |
| `date` | date | yes | Report date in YYYY-MM-DD format. |
| `mode` | string | no | Target scope: exact, prefix, domain, or subdomains. Default: `subdomains`. |
| `volumeMode` | string | no | Search volume calculation mode: monthly or average. Default: `monthly`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "metrics": {
        "org_cost": 1,
        "org_keywords": 1,
        "org_keywords_1_3": 1,
        "org_traffic": 1,
        "paid_cost": 1,
        "paid_keywords": 1,
        "paid_pages": 1,
        "paid_traffic": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `metrics` | object | Site Explorer metrics object. |
| `metrics.org_cost` | number |  |
| `metrics.org_keywords` | number |  |
| `metrics.org_keywords_1_3` | number |  |
| `metrics.org_traffic` | number |  |
| `metrics.paid_cost` | number |  |
| `metrics.paid_keywords` | number |  |
| `metrics.paid_pages` | number |  |
| `metrics.paid_traffic` | number |  |

## Native endpoint

Through the native Ahrefs API, this operation is `GET /site-explorer/metrics` (base URL `https://api.ahrefs.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-site-metrics.md) for the provider-specific parameters and requirements.

