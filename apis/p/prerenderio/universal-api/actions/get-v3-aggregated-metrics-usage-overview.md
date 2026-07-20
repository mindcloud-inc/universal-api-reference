# Prerender.io: List Aggregated Metrics Usage Overview

Retrieves a usage overview from Prerender.io.

```
GET https://connect.mindcloud.co/v1/universal/prerenderio/latest/actions/get-v3-aggregated-metrics-usage-overview
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Prerender.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/prerenderio/latest/actions/get-v3-aggregated-metrics-usage-overview?connectionId=$CONNECTION_ID&domain=string&from=string&timezoneOffset=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "domain": "string",
  "from": "string",
  "timezoneOffset": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/prerenderio/latest/actions/get-v3-aggregated-metrics-usage-overview?${params}`, {
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
      "averageDeliveryTime": 1,
      "crawlBudgetIncrease": 1,
      "maxPagesCached": 1,
      "originalDeliveryTime": 1,
      "pagesRendered": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `averageDeliveryTime` | number |  |
| `crawlBudgetIncrease` | number |  |
| `maxPagesCached` | number |  |
| `originalDeliveryTime` | number |  |
| `pagesRendered` | number |  |

## Native endpoint

Through the native Prerender.io API, this operation is `GET /v3/aggregated-metrics/usage-overview` (base URL `https://api.prerender.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-v3-aggregated-metrics-usage-overview.md) for the provider-specific parameters and requirements.

