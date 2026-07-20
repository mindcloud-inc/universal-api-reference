# SE Ranking Data: Get backlink summary

Retrieves a backlink summary from SE Ranking Data.

```
GET https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/get-backlink-summary
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SE Ranking Data `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/get-backlink-summary?connectionId=$CONNECTION_ID&target=seranking.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "target": "seranking.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/get-backlink-summary?${params}`, {
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
| `mode` | string | no | Target type: domain, subdomain, URL, or exact URL. |
| `target` | string | yes | Target domain or URL to analyze (for example: seranking.com). Example: `seranking.com`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "summary": [
        {
          "anchors": 1,
          "backlinks": 1,
          "dofollowAnchors": 1,
          "dofollowBacklinks": 1,
          "dofollowFromHomePageBacklinks": 1,
          "dofollowRefdomains": 1,
          "domainInlinkRank": 1,
          "eduBacklinks": 1,
          "eduRefdomains": 1,
          "fromHomePageBacklinks": 1,
          "fromHomePageRefdomains": 1,
          "govBacklinks": 1,
          "govRefdomains": 1,
          "inlinkRank": 1,
          "ips": 1,
          "nofollowBacklinks": 1,
          "pagesWithBacklinks": 1,
          "refdomains": 1,
          "subnets": 1,
          "target": "string",
          "textBacklinks": 1,
          "topAnchorsByBacklinks": [
            {
              "anchor": "https://example.com",
              "backlinks": 1
            }
          ],
          "topAnchorsByRefdomains": [
            {
              "anchor": "string",
              "refdomains": 1
            }
          ],
          "topCountries": [
            {
              "count": 1,
              "country": "string"
            }
          ],
          "topPagesByBacklinks": [
            {
              "backlinks": 1,
              "url": "https://example.com"
            }
          ],
          "topPagesByRefdomains": [
            {
              "refdomains": 1,
              "url": "https://example.com"
            }
          ],
          "topTlds": [
            {
              "count": 1,
              "tld": "string"
            }
          ]
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
| `summary` | array<object> | Backlink summary rows. |
| `summary[].anchors` | number |  |
| `summary[].backlinks` | number |  |
| `summary[].dofollowAnchors` | number |  |
| `summary[].dofollowBacklinks` | number |  |
| `summary[].dofollowFromHomePageBacklinks` | number |  |
| `summary[].dofollowRefdomains` | number |  |
| `summary[].domainInlinkRank` | number |  |
| `summary[].eduBacklinks` | number |  |
| `summary[].eduRefdomains` | number |  |
| `summary[].fromHomePageBacklinks` | number |  |
| `summary[].fromHomePageRefdomains` | number |  |
| `summary[].govBacklinks` | number |  |
| `summary[].govRefdomains` | number |  |
| `summary[].inlinkRank` | number |  |
| `summary[].ips` | number |  |
| `summary[].nofollowBacklinks` | number |  |
| `summary[].pagesWithBacklinks` | number |  |
| `summary[].refdomains` | number |  |
| `summary[].subnets` | number |  |
| `summary[].target` | string |  |
| `summary[].textBacklinks` | number |  |
| `summary[].topAnchorsByBacklinks` | array<object> |  |
| `summary[].topAnchorsByBacklinks[]` | object |  |
| `summary[].topAnchorsByBacklinks[].anchor` | string |  |
| `summary[].topAnchorsByBacklinks[].backlinks` | number |  |
| `summary[].topAnchorsByRefdomains` | array<object> |  |
| `summary[].topAnchorsByRefdomains[]` | object |  |
| `summary[].topAnchorsByRefdomains[].anchor` | string |  |
| `summary[].topAnchorsByRefdomains[].refdomains` | number |  |
| `summary[].topCountries` | array<object> |  |
| `summary[].topCountries[]` | object |  |
| `summary[].topCountries[].count` | number |  |
| `summary[].topCountries[].country` | string |  |
| `summary[].topPagesByBacklinks` | array<object> |  |
| `summary[].topPagesByBacklinks[]` | object |  |
| `summary[].topPagesByBacklinks[].backlinks` | number |  |
| `summary[].topPagesByBacklinks[].url` | string |  |
| `summary[].topPagesByRefdomains` | array<object> |  |
| `summary[].topPagesByRefdomains[]` | object |  |
| `summary[].topPagesByRefdomains[].refdomains` | number |  |
| `summary[].topPagesByRefdomains[].url` | string |  |
| `summary[].topTlds` | array<object> |  |
| `summary[].topTlds[]` | object |  |
| `summary[].topTlds[].count` | number |  |
| `summary[].topTlds[].tld` | string |  |

## Native endpoint

Through the native SE Ranking Data API, this operation is `GET /backlinks/summary` (base URL `https://api.seranking.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-backlink-summary.md) for the provider-specific parameters and requirements.

