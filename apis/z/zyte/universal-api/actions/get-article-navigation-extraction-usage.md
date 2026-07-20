# Zyte: Get Article Navigation Extraction Usage

Retrieves article navigation extraction usage metrics from Zyte.

```
GET https://connect.mindcloud.co/v1/universal/zyte/latest/actions/get-article-navigation-extraction-usage
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zyte `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zyte/latest/actions/get-article-navigation-extraction-usage?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zyte/latest/actions/get-article-navigation-extraction-usage?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "page": 1,
      "pageSize": 1,
      "results": [
        {
          "costMicrousdAvg": 1,
          "costMicrousdP80": 1,
          "costMicrousdTotal": 1,
          "day": "2026-05-07T12:00:00.000Z",
          "domain": "string",
          "domainHealth": {
            "globalAvgSuccessRate24h": "string",
            "globalAvgSuccessRate7d": "string",
            "myAvgPriceMicrousd24h": "string",
            "myAvgPriceMicrousd7d": "string",
            "myAvgResponseTime24h": "string",
            "myAvgResponseTime7d": "string",
            "myRequests24h": 1,
            "myRequests7d": 1,
            "mySuccessRate24h": "string",
            "mySuccessRate7d": "string",
            "status": "string",
            "totalSpentMicrousd24h": "string",
            "totalSpentMicrousd7d": "string",
            "totalSuccessfulRequests24h": 1,
            "totalSuccessfulRequests7d": 1
          },
          "hour": "2026-05-07T12:00:00.000Z",
          "month": "2026-05-07T12:00:00.000Z",
          "organizationId": 1,
          "requestCount": 1,
          "responseTimeSecAvg": 1,
          "responseTimeSecP80": 1,
          "statusCodes": [
            {
              "code": 1,
              "count": 1
            }
          ],
          "year": "2026-05-07T12:00:00.000Z"
        }
      ],
      "totalResultCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `page` | number |  |
| `pageSize` | number |  |
| `results[].costMicrousdAvg` | number |  |
| `results[].costMicrousdP80` | number |  |
| `results[].costMicrousdTotal` | number |  |
| `results[].day` | date |  |
| `results[].domain` | string |  |
| `results[].domainHealth.globalAvgSuccessRate24h` | string |  |
| `results[].domainHealth.globalAvgSuccessRate7d` | string |  |
| `results[].domainHealth.myAvgPriceMicrousd24h` | string |  |
| `results[].domainHealth.myAvgPriceMicrousd7d` | string |  |
| `results[].domainHealth.myAvgResponseTime24h` | string |  |
| `results[].domainHealth.myAvgResponseTime7d` | string |  |
| `results[].domainHealth.myRequests24h` | number |  |
| `results[].domainHealth.myRequests7d` | number |  |
| `results[].domainHealth.mySuccessRate24h` | string |  |
| `results[].domainHealth.mySuccessRate7d` | string |  |
| `results[].domainHealth.status` | string |  |
| `results[].domainHealth.totalSpentMicrousd24h` | string |  |
| `results[].domainHealth.totalSpentMicrousd7d` | string |  |
| `results[].domainHealth.totalSuccessfulRequests24h` | number |  |
| `results[].domainHealth.totalSuccessfulRequests7d` | number |  |
| `results[].hour` | date |  |
| `results[].month` | date |  |
| `results[].organizationId` | number |  |
| `results[].requestCount` | number |  |
| `results[].responseTimeSecAvg` | number |  |
| `results[].responseTimeSecP80` | number |  |
| `results[].statusCodes[].code` | number |  |
| `results[].statusCodes[].count` | number |  |
| `results[].year` | date |  |
| `totalResultCount` | number |  |

## Native endpoint

Through the native Zyte API, this operation is `GET /api/stats` (base URL `https://zyte-api-stats.zyte.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-article-navigation-extraction-usage.md) for the provider-specific parameters and requirements.

