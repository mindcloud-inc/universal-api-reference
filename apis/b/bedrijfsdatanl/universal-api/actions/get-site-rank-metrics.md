# Bedrijfsdata.nl: Get Site Rank Metrics



```
GET https://connect.mindcloud.co/v1/universal/bedrijfsdatanl/latest/actions/get-site-rank-metrics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bedrijfsdata.nl `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bedrijfsdatanl/latest/actions/get-site-rank-metrics?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bedrijfsdatanl/latest/actions/get-site-rank-metrics?${params}`, {
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
| `domain` | string | no | Domain to evaluate for site metrics. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "backlinkDomains": 1,
      "backlinks": 1,
      "bounceRate": 1,
      "creditsUsed": 1,
      "creditsUsedMonth": 1,
      "domain": "string",
      "homepageMobileResources": 1,
      "homepageMobileTiming": 1,
      "indexableUrls": 1,
      "monthlyCredits": 1,
      "monthlyVisits": 1,
      "pagerank": 1,
      "pagespeedMobileScore": {
        "accessibility": 1,
        "bestPractices": 1,
        "performance": 1,
        "seo": 1
      },
      "product": "string",
      "rankings": [
        {
          "name": "Ava Chen",
          "perc": 1,
          "percList": 1,
          "rank": 1
        }
      ],
      "status": "string",
      "timeOnSite": 1,
      "url": "https://example.com",
      "visitedPages": 1,
      "webrankHistory": [
        {
          "date": "2026-05-07T12:00:00.000Z",
          "perc": 1,
          "time": "2026-05-07T12:00:00.000Z",
          "webrank": 1
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `backlinkDomains` | number |  |
| `backlinks` | number |  |
| `bounceRate` | number |  |
| `creditsUsed` | number |  |
| `creditsUsedMonth` | number |  |
| `domain` | string |  |
| `homepageMobileResources` | number |  |
| `homepageMobileTiming` | number |  |
| `indexableUrls` | number |  |
| `monthlyCredits` | number |  |
| `monthlyVisits` | number |  |
| `pagerank` | number |  |
| `pagespeedMobileScore.accessibility` | number |  |
| `pagespeedMobileScore.bestPractices` | number |  |
| `pagespeedMobileScore.performance` | number |  |
| `pagespeedMobileScore.seo` | number |  |
| `product` | string |  |
| `rankings[].name` | string |  |
| `rankings[].perc` | number |  |
| `rankings[].percList` | number |  |
| `rankings[].rank` | number |  |
| `status` | string |  |
| `timeOnSite` | number |  |
| `url` | string |  |
| `visitedPages` | number |  |
| `webrankHistory[].date` | date |  |
| `webrankHistory[].perc` | number |  |
| `webrankHistory[].time` | date |  |
| `webrankHistory[].webrank` | number |  |

## Native endpoint

Through the native Bedrijfsdata.nl API, this operation is `GET /siterank` (base URL `https://fapi.bedrijfsdata.nl/v1.2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-site-rank-metrics.md) for the provider-specific parameters and requirements.

