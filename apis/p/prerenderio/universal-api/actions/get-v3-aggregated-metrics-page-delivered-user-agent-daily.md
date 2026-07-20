# Prerender.io: List Aggregated Metrics Page Delivered User Agent Daily

Retrieves daily delivered page user agent metrics from Prerender.io.

```
GET https://connect.mindcloud.co/v1/universal/prerenderio/latest/actions/get-v3-aggregated-metrics-page-delivered-user-agent-daily
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Prerender.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/prerenderio/latest/actions/get-v3-aggregated-metrics-page-delivered-user-agent-daily?connectionId=$CONNECTION_ID&domain=string&from=string&timezoneOffset=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "domain": "string",
  "from": "string",
  "timezoneOffset": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/prerenderio/latest/actions/get-v3-aggregated-metrics-page-delivered-user-agent-daily?${params}`, {
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
| `domain` | string | yes |  |
| `from` | string | yes |  |
| `timezoneOffset` | number | yes | Time zone offset in minutes |

## Response

```json
{
  "success": true,
  "data": [
    {
      "AdsbotGoogle": 1,
      "Ahrefsbot": 1,
      "Applebot": 1,
      "Bingbot": 1,
      "day": "string",
      "Facebook": 1,
      "Googlebot": 1,
      "Other": 1,
      "Pinterestbot": 1,
      "Semrushbot": 1,
      "Yandexbot": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `AdsbotGoogle` | number |  |
| `Ahrefsbot` | number |  |
| `Applebot` | number |  |
| `Bingbot` | number |  |
| `day` | string |  |
| `Facebook` | number |  |
| `Googlebot` | number |  |
| `Other` | number |  |
| `Pinterestbot` | number |  |
| `Semrushbot` | number |  |
| `Yandexbot` | number |  |

## Native endpoint

Through the native Prerender.io API, this operation is `GET /v3/aggregated-metrics/page-delivered-user-agent/daily` (base URL `https://api.prerender.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-v3-aggregated-metrics-page-delivered-user-agent-daily.md) for the provider-specific parameters and requirements.

