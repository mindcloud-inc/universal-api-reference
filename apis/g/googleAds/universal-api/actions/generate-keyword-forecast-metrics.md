# Google Ads: Generate Keyword Forecast Metrics

Generates keyword forecast metrics in Google Ads.

```
GET https://connect.mindcloud.co/v1/universal/googleAds/latest/actions/generate-keyword-forecast-metrics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Ads `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleAds/latest/actions/generate-keyword-forecast-metrics?connectionId=$CONNECTION_ID&customerId=1234567890&campaign=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customerId": "1234567890",
  "campaign": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleAds/latest/actions/generate-keyword-forecast-metrics?${params}`, {
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
| `customerId` | list | yes | Customer ID to generate forecast metrics for (without dashes). Example: `1234567890`. |
| `campaign` | object | yes | Campaign definition used for keyword forecast metrics. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "campaignForecastMetrics": {
        "averageCpaMicros": "string",
        "averageCpcMicros": "string",
        "clicks": 1,
        "clickThroughRate": 1,
        "conversionRate": 1,
        "conversions": 1,
        "costMicros": "string",
        "impressions": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `campaignForecastMetrics.averageCpaMicros` | string |  |
| `campaignForecastMetrics.averageCpcMicros` | string |  |
| `campaignForecastMetrics.clicks` | number |  |
| `campaignForecastMetrics.clickThroughRate` | number |  |
| `campaignForecastMetrics.conversionRate` | number |  |
| `campaignForecastMetrics.conversions` | number |  |
| `campaignForecastMetrics.costMicros` | string |  |
| `campaignForecastMetrics.impressions` | number |  |

## Native endpoint

Through the native Google Ads API, this operation is `POST v22/customers/:customerId:generateKeywordForecastMetrics` (base URL `https://googleads.googleapis.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-keyword-forecast-metrics.md) for the provider-specific parameters and requirements.

