# SE Ranking Data: Get all crawled pages

Retrieves all crawled pages from SE Ranking Data.

```
GET https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/get-all-crawled-pages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SE Ranking Data `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/get-all-crawled-pages?connectionId=$CONNECTION_ID&auditId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "auditId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/get-all-crawled-pages?${params}`, {
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
| `auditId` | list<string> | yes | Audit identifier. Example: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "items": [
        {
          "amp": "string",
          "blockedRobots": "string",
          "canonicalUrl": "https://example.com",
          "chars": "string",
          "contentHash": "string",
          "cssSize": "string",
          "depth": "string",
          "description": "string",
          "descriptionDuplicate": "string",
          "descriptionLen": "string",
          "errors": "string",
          "firstMs": "string",
          "h1": "string",
          "h1Duplicate": "string",
          "h1Len": "string",
          "h2": "string",
          "h2Len": "string",
          "h3Count": "string",
          "h4Count": "string",
          "h5Count": "string",
          "h6Count": "string",
          "hreflang": "string",
          "hreflangLink": "https://example.com",
          "htmlRatio": "string",
          "id": "string",
          "img": "string",
          "imgSize": "string",
          "indexable": "string",
          "indexableStatus": "string",
          "inlinks": "https://example.com",
          "inlinksFollow": "https://example.com",
          "inlinksNofollow": "https://example.com",
          "issues": "string",
          "jsSize": "string",
          "loadMs": "string",
          "metaRefresh": "string",
          "nofollow": "string",
          "noindex": "string",
          "notices": "string",
          "numKeywords": "string",
          "outlinksExternal": "https://example.com",
          "outlinksInternal": "https://example.com",
          "redirectCount": "string",
          "redirectLinks": "https://example.com",
          "refpages": "string",
          "robots": "string",
          "singleH1": "string",
          "singleH2": "string",
          "sitemap": "string",
          "size": "string",
          "status": "string",
          "timeCheck": "string",
          "title": "string",
          "titleDuplicate": "string",
          "titleLen": "string",
          "totalLinks": "https://example.com",
          "trafficForecast": "string",
          "type": "string",
          "url": "https://example.com",
          "urlLen": "https://example.com",
          "urlProtocol": "https://example.com",
          "warnings": "string",
          "wordsCount": "string"
        }
      ],
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `items` | array<object> |  |
| `items[].amp` | string |  |
| `items[].blockedRobots` | string |  |
| `items[].canonicalUrl` | string |  |
| `items[].chars` | string |  |
| `items[].contentHash` | string |  |
| `items[].cssSize` | string |  |
| `items[].depth` | string |  |
| `items[].description` | string |  |
| `items[].descriptionDuplicate` | string |  |
| `items[].descriptionLen` | string |  |
| `items[].errors` | string |  |
| `items[].firstMs` | string |  |
| `items[].h1` | string |  |
| `items[].h1Duplicate` | string |  |
| `items[].h1Len` | string |  |
| `items[].h2` | string |  |
| `items[].h2Len` | string |  |
| `items[].h3Count` | string |  |
| `items[].h4Count` | string |  |
| `items[].h5Count` | string |  |
| `items[].h6Count` | string |  |
| `items[].hreflang` | string |  |
| `items[].hreflangLink` | string |  |
| `items[].htmlRatio` | string |  |
| `items[].id` | string |  |
| `items[].img` | string |  |
| `items[].imgSize` | string |  |
| `items[].indexable` | string |  |
| `items[].indexableStatus` | string |  |
| `items[].inlinks` | string |  |
| `items[].inlinksFollow` | string |  |
| `items[].inlinksNofollow` | string |  |
| `items[].issues` | string |  |
| `items[].jsSize` | string |  |
| `items[].loadMs` | string |  |
| `items[].metaRefresh` | string |  |
| `items[].nofollow` | string |  |
| `items[].noindex` | string |  |
| `items[].notices` | string |  |
| `items[].numKeywords` | string |  |
| `items[].outlinksExternal` | string |  |
| `items[].outlinksInternal` | string |  |
| `items[].redirectCount` | string |  |
| `items[].redirectLinks` | string |  |
| `items[].refpages` | string |  |
| `items[].robots` | string |  |
| `items[].singleH1` | string |  |
| `items[].singleH2` | string |  |
| `items[].sitemap` | string |  |
| `items[].size` | string |  |
| `items[].status` | string |  |
| `items[].timeCheck` | string |  |
| `items[].title` | string |  |
| `items[].titleDuplicate` | string |  |
| `items[].titleLen` | string |  |
| `items[].totalLinks` | string |  |
| `items[].trafficForecast` | string |  |
| `items[].type` | string |  |
| `items[].url` | string |  |
| `items[].urlLen` | string |  |
| `items[].urlProtocol` | string |  |
| `items[].warnings` | string |  |
| `items[].wordsCount` | string |  |
| `total` | number |  |

## Native endpoint

Through the native SE Ranking Data API, this operation is `GET /site-audit/audits/pages` (base URL `https://api.seranking.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-all-crawled-pages.md) for the provider-specific parameters and requirements.

