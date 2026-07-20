# Prerender.io: List Aggregated Metrics Page Rendered Status Code Daily

Retrieves daily rendered page status code metrics from Prerender.io.

```
GET https://connect.mindcloud.co/v1/universal/prerenderio/latest/actions/get-v3-aggregated-metrics-page-rendered-status-code-daily
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Prerender.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/prerenderio/latest/actions/get-v3-aggregated-metrics-page-rendered-status-code-daily?connectionId=$CONNECTION_ID&domain=string&from=string&timezoneOffset=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "domain": "string",
  "from": "string",
  "timezoneOffset": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/prerenderio/latest/actions/get-v3-aggregated-metrics-page-rendered-status-code-daily?${params}`, {
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
      "day": "string",
      "statusCode2xx": 1,
      "statusCode301": 1,
      "statusCode302": 1,
      "statusCode307": 1,
      "statusCode308": 1,
      "statusCode3xx": 1,
      "statusCode401": 1,
      "statusCode403": 1,
      "statusCode404": 1,
      "statusCode410": 1,
      "statusCode429": 1,
      "statusCode4xx": 1,
      "statusCode503": 1,
      "statusCode504": 1,
      "statusCode5xx": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `day` | string |  |
| `statusCode2xx` | number |  |
| `statusCode301` | number |  |
| `statusCode302` | number |  |
| `statusCode307` | number |  |
| `statusCode308` | number |  |
| `statusCode3xx` | number |  |
| `statusCode401` | number |  |
| `statusCode403` | number |  |
| `statusCode404` | number |  |
| `statusCode410` | number |  |
| `statusCode429` | number |  |
| `statusCode4xx` | number |  |
| `statusCode503` | number |  |
| `statusCode504` | number |  |
| `statusCode5xx` | number |  |

## Native endpoint

Through the native Prerender.io API, this operation is `GET /v3/aggregated-metrics/page-rendered-status-code/daily` (base URL `https://api.prerender.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-v3-aggregated-metrics-page-rendered-status-code-daily.md) for the provider-specific parameters and requirements.

