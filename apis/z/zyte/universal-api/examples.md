# Zyte Universal API Examples

These examples use the MindCloud API key and Zyte connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Usage Overview

Retrieves usage overview metrics from Zyte.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zyte/latest/actions/get-usage-overview?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zyte/latest/actions/get-usage-overview?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

Example response:

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

See the full [Get Usage Overview action reference](actions/get-usage-overview.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/zyte/latest/actions/get-usage-overview).
