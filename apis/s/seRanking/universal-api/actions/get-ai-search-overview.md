# SE Ranking Data: Get AI search overview

Retrieves AI search overview data from SE Ranking Data.

```
GET https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/get-ai-search-overview
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SE Ranking Data `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/get-ai-search-overview?connectionId=$CONNECTION_ID&engine=chatgpt&scope=base_domain&source=us&target=seranking.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "engine": "chatgpt",
  "scope": "base_domain",
  "source": "us",
  "target": "seranking.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/get-ai-search-overview?${params}`, {
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
| `endDate` | string | no | End date in YYYY-MM-DD format. |
| `engine` | list<string> | yes | Engine identifier (for example: chatgpt). One of: `ai_overview`, `chatgpt`. Example: `chatgpt`. |
| `scope` | list<string> | yes | Analysis scope: domain, base_domain, subdomain, exact_url, or path. One of: `base_domain`, `domain`, `exact_url`, `path`, `subdomain`. Example: `base_domain`. |
| `source` | string | yes | Regional source code (for example: us). Example: `us`. |
| `startDate` | string | no | Start date in YYYY-MM-DD format. |
| `target` | string | yes | Target domain or URL (for example: seranking.com). Example: `seranking.com`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "summary": {
        "aiOpportunityTraffic": {
          "changeAbsolute": 1,
          "changePercent": 1,
          "current": 1
        },
        "averagePosition": {
          "current": 1
        },
        "brandPresence": {
          "changeAbsolute": 1,
          "changePercent": 1,
          "current": 1
        },
        "linkPresence": {
          "changeAbsolute": 1,
          "changePercent": 1,
          "current": 1
        }
      },
      "timeSeries": {
        "aiTraffic": [
          "string"
        ],
        "averagePosition": [
          "string"
        ],
        "linkPresence": [
          "https://example.com"
        ],
        "organicTraffic": [
          "string"
        ],
        "overallTraffic": [
          "string"
        ]
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `summary` | object | Aggregate AI visibility metrics for the selected target and engine. |
| `summary.aiOpportunityTraffic` | object |  |
| `summary.aiOpportunityTraffic.changeAbsolute` | number |  |
| `summary.aiOpportunityTraffic.changePercent` | number |  |
| `summary.aiOpportunityTraffic.current` | number |  |
| `summary.averagePosition` | object |  |
| `summary.averagePosition.current` | number |  |
| `summary.brandPresence` | object |  |
| `summary.brandPresence.changeAbsolute` | number |  |
| `summary.brandPresence.changePercent` | number |  |
| `summary.brandPresence.current` | number |  |
| `summary.linkPresence` | object |  |
| `summary.linkPresence.changeAbsolute` | number |  |
| `summary.linkPresence.changePercent` | number |  |
| `summary.linkPresence.current` | number |  |
| `timeSeries` | object | Time-series metric collections keyed by metric name. |
| `timeSeries.aiTraffic` | array<string> |  |
| `timeSeries.averagePosition` | array<string> |  |
| `timeSeries.linkPresence` | array<string> |  |
| `timeSeries.organicTraffic` | array<string> |  |
| `timeSeries.overallTraffic` | array<string> |  |

## Native endpoint

Through the native SE Ranking Data API, this operation is `GET /ai-search/overview/by-engine/time-series` (base URL `https://api.seranking.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-ai-search-overview.md) for the provider-specific parameters and requirements.

