# Prerender.io: List Aggregated Metrics Pages Crawled Volume

Retrieves pages crawled volume metrics from Prerender.io.

```
GET https://connect.mindcloud.co/v1/universal/prerenderio/latest/actions/get-v4-aggregated-metrics-pages-crawled-volume
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Prerender.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/prerenderio/latest/actions/get-v4-aggregated-metrics-pages-crawled-volume?connectionId=$CONNECTION_ID&crawlers=string&dateFrom=string&dateTo=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "crawlers": "string",
  "dateFrom": "string",
  "dateTo": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/prerenderio/latest/actions/get-v4-aggregated-metrics-pages-crawled-volume?${params}`, {
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
| `crawlers` | list<string> | yes |  |
| `dateFrom` | string | yes |  |
| `dateTo` | string | yes |  |
| `domain` | string | no |  |
| `firstDayOfWeek` | number | no | First day of the week (0 = Sunday, 1 = Monday, etc.) |
| `timezone` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "value": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | object |  |

## Native endpoint

Through the native Prerender.io API, this operation is `GET /v4/aggregated-metrics/pages-crawled-volume` (base URL `https://api.prerender.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-v4-aggregated-metrics-pages-crawled-volume.md) for the provider-specific parameters and requirements.

