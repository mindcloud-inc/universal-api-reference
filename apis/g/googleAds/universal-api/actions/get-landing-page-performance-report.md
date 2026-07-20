# Google Ads: Get Landing Page Performance Report

Retrieves a landing page performance report from Google Ads.

```
GET https://connect.mindcloud.co/v1/universal/googleAds/latest/actions/get-landing-page-performance-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Ads `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleAds/latest/actions/get-landing-page-performance-report?connectionId=$CONNECTION_ID&customerId=1234567890" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customerId": "1234567890"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleAds/latest/actions/get-landing-page-performance-report?${params}`, {
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
| `customerId` | list | yes | Customer ID to query (without dashes). Example: `1234567890`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `startDate` | string | no | Optional start date (YYYY-MM-DD). Example: `2026-02-01`. |
| `endDate` | string | no | Optional end date (YYYY-MM-DD). Example: `2026-02-28`. |
| `filterClause` | string | no | Optional GAQL filter clause fragment without WHERE (advanced). Example: `metrics.clicks > 10`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "adGroup": {
        "id": "string",
        "name": "Ava Chen",
        "resourceName": "Ava Chen"
      },
      "campaign": {
        "id": "string",
        "name": "Ava Chen",
        "resourceName": "Ava Chen"
      },
      "landingPageView": {
        "resourceName": "Ava Chen",
        "unexpandedFinalUrl": "https://example.com"
      },
      "metrics": {
        "clicks": "string",
        "conversions": 1,
        "costMicros": "string",
        "impressions": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `adGroup.id` | string |  |
| `adGroup.name` | string |  |
| `adGroup.resourceName` | string |  |
| `campaign.id` | string |  |
| `campaign.name` | string |  |
| `campaign.resourceName` | string |  |
| `landingPageView.resourceName` | string |  |
| `landingPageView.unexpandedFinalUrl` | string |  |
| `metrics.clicks` | string |  |
| `metrics.conversions` | number |  |
| `metrics.costMicros` | string |  |
| `metrics.impressions` | string |  |

## Native endpoint

Through the native Google Ads API, this operation is `POST v22/customers/:customerId/googleAds:search` (base URL `https://googleads.googleapis.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-landing-page-performance-report.md) for the provider-specific parameters and requirements.

