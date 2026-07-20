# Google Ads: Search Google Ads

Searches Google Ads using a custom GAQL query.

```
GET https://connect.mindcloud.co/v1/universal/googleAds/latest/actions/search-google-ads
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Ads `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleAds/latest/actions/search-google-ads?connectionId=$CONNECTION_ID&customerId=1234567890&query=SELECT%20campaign.id%2C%20campaign.name%2C%20metrics.impressions%2C%20metrics.clicks%2C%20metrics.cost_micros%20FROM%20campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customerId": "1234567890",
  "query": "SELECT campaign.id, campaign.name, metrics.impressions, metrics.clicks, metrics.cost_micros FROM campaign"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleAds/latest/actions/search-google-ads?${params}`, {
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
| `query` | string | yes | GAQL query to execute. Use field names from the Google Ads Fields reference. Default: `SELECT campaign.id, campaign.name, metrics.impressions, metrics.clicks, metrics.cost_micros FROM campaign`. Example: `SELECT campaign.id, campaign.name, metrics.impressions, metrics.clicks, metrics.cost_micros FROM campaign`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `startDate` | string | no | Optional start date for automatic segments.date filter (YYYY-MM-DD). Example: `2026-02-01`. |
| `endDate` | string | no | Optional end date for automatic segments.date filter (YYYY-MM-DD). Example: `2026-02-28`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "customer": {
        "descriptiveName": "Ava Chen",
        "id": "string",
        "resourceName": "Ava Chen"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `customer.descriptiveName` | string |  |
| `customer.id` | string |  |
| `customer.resourceName` | string |  |

## Native endpoint

Through the native Google Ads API, this operation is `POST v22/customers/:customerId/googleAds:search` (base URL `https://googleads.googleapis.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-google-ads.md) for the provider-specific parameters and requirements.

