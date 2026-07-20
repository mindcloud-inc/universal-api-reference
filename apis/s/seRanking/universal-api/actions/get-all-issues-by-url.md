# SE Ranking Data: Get all issues by URL

Retrieves all issues by URL from SE Ranking Data.

```
GET https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/get-all-issues-by-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SE Ranking Data `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/get-all-issues-by-url?connectionId=$CONNECTION_ID&auditId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "auditId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/get-all-issues-by-url?${params}`, {
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
| `url` | string | no | Specific URL to fetch issue details for. Example: `https://seranking.com/`. |
| `urlId` | string | no | Numeric URL identifier returned by audit pages endpoint. Example: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "issues": [
        {
          "code": "string",
          "group": "string",
          "snippet": {
            "type": "string",
            "value": [
              {
                "status": "string",
                "url": "https://example.com"
              }
            ]
          },
          "type": "string"
        }
      ],
      "pageData": {
        "canonical": "string",
        "chars": 1,
        "css": 1,
        "cssSize": 1,
        "description": "string",
        "descriptionHash": "string",
        "descriptionLen": 1,
        "doc": 1,
        "encoding": "string",
        "extDoc": 1,
        "extJs": 1,
        "h1": "string",
        "h1Count": 1,
        "h1Hash": "string",
        "h1Len": 1,
        "h2": "string",
        "h2Count": 1,
        "h2Len": 1,
        "h3Count": 1,
        "hreflang": {
          "de": "string",
          "en": "string",
          "es": "string",
          "fr": "string",
          "it": "string",
          "ja": "string",
          "nl": "string",
          "pt": "string",
          "ru": "string",
          "uk": "string",
          "xDefault": "string"
        },
        "htmlRatio": 1,
        "img": 1,
        "imgSize": 1,
        "inlinks": 1,
        "issuesCount": 1,
        "js": 1,
        "jsSize": 1,
        "lang": "string",
        "noticesCount": 1,
        "numKeywords": 1,
        "refpages": 1,
        "robots": "string",
        "timeCheck": "string",
        "title": "string",
        "titleHash": "string",
        "titleLen": 1,
        "totalLinks": 1,
        "trafficForecast": 1,
        "warningsCount": 1,
        "words": 1
      },
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `issues` | array<object> |  |
| `issues[].code` | string |  |
| `issues[].group` | string |  |
| `issues[].snippet` | object |  |
| `issues[].snippet.type` | string |  |
| `issues[].snippet.value` | array<object> |  |
| `issues[].snippet.value[]` | object |  |
| `issues[].snippet.value[].status` | string |  |
| `issues[].snippet.value[].url` | string |  |
| `issues[].type` | string |  |
| `pageData` | object |  |
| `pageData.canonical` | string |  |
| `pageData.chars` | number |  |
| `pageData.css` | number |  |
| `pageData.cssSize` | number |  |
| `pageData.description` | string |  |
| `pageData.descriptionHash` | string |  |
| `pageData.descriptionLen` | number |  |
| `pageData.doc` | number |  |
| `pageData.encoding` | string |  |
| `pageData.extDoc` | number |  |
| `pageData.extJs` | number |  |
| `pageData.h1` | string |  |
| `pageData.h1Count` | number |  |
| `pageData.h1Hash` | string |  |
| `pageData.h1Len` | number |  |
| `pageData.h2` | string |  |
| `pageData.h2Count` | number |  |
| `pageData.h2Len` | number |  |
| `pageData.h3Count` | number |  |
| `pageData.hreflang` | object |  |
| `pageData.hreflang.de` | string |  |
| `pageData.hreflang.en` | string |  |
| `pageData.hreflang.es` | string |  |
| `pageData.hreflang.fr` | string |  |
| `pageData.hreflang.it` | string |  |
| `pageData.hreflang.ja` | string |  |
| `pageData.hreflang.nl` | string |  |
| `pageData.hreflang.pt` | string |  |
| `pageData.hreflang.ru` | string |  |
| `pageData.hreflang.uk` | string |  |
| `pageData.hreflang.xDefault` | string |  |
| `pageData.htmlRatio` | number |  |
| `pageData.img` | number |  |
| `pageData.imgSize` | number |  |
| `pageData.inlinks` | number |  |
| `pageData.issuesCount` | number |  |
| `pageData.js` | number |  |
| `pageData.jsSize` | number |  |
| `pageData.lang` | string |  |
| `pageData.noticesCount` | number |  |
| `pageData.numKeywords` | number |  |
| `pageData.refpages` | number |  |
| `pageData.robots` | string |  |
| `pageData.timeCheck` | string |  |
| `pageData.title` | string |  |
| `pageData.titleHash` | string |  |
| `pageData.titleLen` | number |  |
| `pageData.totalLinks` | number |  |
| `pageData.trafficForecast` | number |  |
| `pageData.warningsCount` | number |  |
| `pageData.words` | number |  |
| `url` | string |  |

## Native endpoint

Through the native SE Ranking Data API, this operation is `GET /site-audit/audits/issues` (base URL `https://api.seranking.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-all-issues-by-url.md) for the provider-specific parameters and requirements.

