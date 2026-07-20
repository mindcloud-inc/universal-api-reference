# SE Ranking Project: Get Project Summary Statistics

Retrieves project summary statistics from SE Ranking.

```
GET https://connect.mindcloud.co/v1/universal/sERankingProject/latest/actions/get-project-summary-statistics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SE Ranking Project `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sERankingProject/latest/actions/get-project-summary-statistics?connectionId=$CONNECTION_ID&site_id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "site_id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sERankingProject/latest/actions/get-project-summary-statistics?${params}`, {
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
| `site_id` | list<number> | yes | Project site identifier from SE Ranking. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "domainTrust": 1,
      "indexGoogle": "string",
      "process": 1,
      "siteId": 1,
      "todayAvg": 1,
      "top10": 1,
      "top30": 1,
      "top5": 1,
      "totalDown": 1,
      "totalUp": 1,
      "visibility": 1,
      "visibilityPercent": 1,
      "yesterdayAvg": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `domainTrust` | number |  |
| `indexGoogle` | string |  |
| `process` | number |  |
| `siteId` | number |  |
| `todayAvg` | number |  |
| `top10` | number |  |
| `top30` | number |  |
| `top5` | number |  |
| `totalDown` | number |  |
| `totalUp` | number |  |
| `visibility` | number |  |
| `visibilityPercent` | number |  |
| `yesterdayAvg` | number |  |

## Native endpoint

Through the native SE Ranking Project API, this operation is `GET /sites/:site_id/stat` (base URL `https://api4.seranking.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project-summary-statistics.md) for the provider-specific parameters and requirements.

