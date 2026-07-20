# Google Ads: Generate Keyword Historical Metrics

Generates keyword historical metrics in Google Ads.

```
GET https://connect.mindcloud.co/v1/universal/googleAds/latest/actions/generate-keyword-historical-metrics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Ads `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleAds/latest/actions/generate-keyword-historical-metrics?connectionId=$CONNECTION_ID&customerId=1234567890&keywords%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customerId": "1234567890",
  "keywords[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleAds/latest/actions/generate-keyword-historical-metrics?${params}`, {
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
| `customerId` | list | yes | Customer ID to generate historical metrics for (without dashes). Example: `1234567890`. |
| `keywords[]` | array<string> | yes | Keywords for historical metrics lookup. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `language` | string | no | Resource name of the language constant. Example: `languageConstants/1000`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "keywordMetrics": {
        "avgMonthlySearches": "string",
        "competition": "string",
        "competitionIndex": "string",
        "highTopOfPageBidMicros": "string",
        "lowTopOfPageBidMicros": "string",
        "monthlySearchVolumes": [
          {
            "month": "string",
            "monthlySearches": "string",
            "year": "string"
          }
        ]
      },
      "text": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `keywordMetrics.avgMonthlySearches` | string |  |
| `keywordMetrics.competition` | string |  |
| `keywordMetrics.competitionIndex` | string |  |
| `keywordMetrics.highTopOfPageBidMicros` | string |  |
| `keywordMetrics.lowTopOfPageBidMicros` | string |  |
| `keywordMetrics.monthlySearchVolumes[].month` | string |  |
| `keywordMetrics.monthlySearchVolumes[].monthlySearches` | string |  |
| `keywordMetrics.monthlySearchVolumes[].year` | string |  |
| `text` | string |  |

## Native endpoint

Through the native Google Ads API, this operation is `POST v22/customers/:customerId:generateKeywordHistoricalMetrics` (base URL `https://googleads.googleapis.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-keyword-historical-metrics.md) for the provider-specific parameters and requirements.

