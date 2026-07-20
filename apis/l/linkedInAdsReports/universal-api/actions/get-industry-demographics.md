# LinkedIn Ads Reports: Get Industry Demographics

Retrieves industry demographics from LinkedIn Ads Reports.

```
GET https://connect.mindcloud.co/v1/universal/linkedInAdsReports/latest/actions/get-industry-demographics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LinkedIn Ads Reports `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/linkedInAdsReports/latest/actions/get-industry-demographics?connectionId=$CONNECTION_ID&facet=accounts%3DList(urn%253Ali%253AsponsoredAccount%253A123456)&startYear=2026&startMonth=4&startDay=1&endYear=2026&endMonth=4&endDay=26&timeGranularity=DAILY" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "facet": "accounts=List(urn%3Ali%3AsponsoredAccount%3A123456)",
  "startYear": "2026",
  "startMonth": "4",
  "startDay": "1",
  "endYear": "2026",
  "endMonth": "4",
  "endDay": "26",
  "timeGranularity": "DAILY"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/linkedInAdsReports/latest/actions/get-industry-demographics?${params}`, {
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
| `facet` | string | yes | LinkedIn account facet expression, for example accounts=List(urn%3Ali%3AsponsoredAccount%3A123456). Default: `accounts=List(urn%3Ali%3AsponsoredAccount%3A123456)`. |
| `startYear` | number | yes | Start date year. Default: `2026`. |
| `startMonth` | number | yes | Start date month. Default: `4`. |
| `startDay` | number | yes | Start date day. Default: `1`. |
| `endYear` | number | yes | End date year. Default: `2026`. |
| `endMonth` | number | yes | End date month. Default: `4`. |
| `endDay` | number | yes | End date day. Default: `26`. |
| `timeGranularity` | string | yes | Time grouping for the report, such as DAILY or ALL. Default: `DAILY`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "clicks": 1,
      "costInLocalCurrency": 1,
      "dateRange": {},
      "impressions": 1,
      "pivotValues": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `clicks` | number |  |
| `costInLocalCurrency` | number |  |
| `dateRange` | object |  |
| `impressions` | number |  |
| `pivotValues` | array<string> |  |

## Native endpoint

Through the native LinkedIn Ads Reports API, this operation is `GET /rest/adAnalytics?q=analytics&pivot=MEMBER_INDUSTRY&dateRange=(start:(year:{{startYear}},month:{{startMonth}},day:{{startDay}}),end:(year:{{endYear}},month:{{endMonth}},day:{{endDay}}))&timeGranularity={{timeGranularity}}&{{facet}}` (base URL `https://api.linkedin.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-industry-demographics.md) for the provider-specific parameters and requirements.

