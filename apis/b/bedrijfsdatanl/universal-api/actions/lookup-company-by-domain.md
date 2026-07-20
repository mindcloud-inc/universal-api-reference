# Bedrijfsdata.nl: Lookup Company By Domain



```
GET https://connect.mindcloud.co/v1/universal/bedrijfsdatanl/latest/actions/lookup-company-by-domain
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bedrijfsdata.nl `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bedrijfsdatanl/latest/actions/lookup-company-by-domain?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bedrijfsdatanl/latest/actions/lookup-company-by-domain?${params}`, {
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
| `domain` | string | no | Domain to analyze with RAG. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "creditsUsed": 1,
      "creditsUsedMonth": 1,
      "domain": "string",
      "monthlyCredits": 1,
      "pages": {
        "all": {
          "article": "string",
          "articleSum": "string",
          "contentall": "string",
          "contentSum": "string",
          "introduction": "string",
          "metaarticle": "string",
          "metaarticleSum": "string",
          "title": "string"
        },
        "home": {
          "alt": [
            "string"
          ],
          "article": "string",
          "articledigest": "string",
          "articledivCount": 1,
          "articleFoot": "string",
          "articleFootNormal": 1,
          "articleHead": "string",
          "articleimageCount": 1,
          "articlelength": 1,
          "articlelengthOrg": 1,
          "articlelinesCount": 1,
          "articlelineslong": 1,
          "articlestart": [
            "string"
          ],
          "articleSum": "string",
          "base": "string",
          "bodyBase": "string",
          "bodyDomain": "string",
          "bodyHost": "string",
          "bodylength": 1,
          "bodyUrl": "https://example.com",
          "cacheFile": "string",
          "cleanArticle": "string",
          "content": "string",
          "contentall": "string",
          "contentallSum": "string",
          "contentdigest": "string",
          "contentlength": 1,
          "contentnoboiler": "string",
          "contentSum": "string",
          "domain": "string",
          "firstText": "string",
          "footer": "string",
          "formcount": 1,
          "frameraw": [
            "string"
          ],
          "fromCache": 1,
          "h1": [
            "string"
          ],
          "head": "string",
          "headLang": "string",
          "headlength": 1,
          "headsplit": "string",
          "headsplitStart": "string",
          "homepageHtml": "string",
          "host": "string",
          "htmlArticleSection": 1,
          "htmlHeaderSection": 1,
          "httpCode": 1,
          "httpEquivXUaCompatible": "string",
          "iframescount": 1,
          "imagescount": 1,
          "internallinksactive": 1,
          "introduction": "string",
          "introductiondigest": "string",
          "l": 1,
          "lang": "string",
          "linkArticleEnd": 1,
          "linkArticleEndInternal": 1,
          "linkArticleStart": 1,
          "linkArticleStartInternal": 1,
          "linkContentEnd": 1,
          "linkContentEndInternal": 1,
          "linkContentStart": 1,
          "linkContentStartInternal": 1,
          "linkCount": 1,
          "linkdomain": [
            "https://example.com"
          ],
          "linkraw": [
            "https://example.com"
          ],
          "linksactive": 1,
          "linksanchor": [
            "https://example.com"
          ],
          "linksinarticleCount": 1,
          "linksnofollow": [
            1
          ],
          "linkstitle": [
            "https://example.com"
          ],
          "logoAlt": "string",
          "logoSrc": "string",
          "metaarticle": "string",
          "metaarticleRaw": "string",
          "metaarticleSum": "string",
          "metaCharset": "string",
          "metaEncoding": "string",
          "metaMsapplicationSquare150x150logo": "string",
          "metaMsapplicationSquare310x310logo": "string",
          "metaMsapplicationSquare70x70logo": "string",
          "metaMsapplicationTilecolor": "string",
          "metaMsapplicationWide310x150logo": "string",
          "metaViewport": "string",
          "outlinks": 1,
          "pagetitle": "string",
          "pagetitleMatch": "string",
          "path": "string",
          "pathClean": "string",
          "pathqueryClean": "string",
          "propertyOgSiteName": "Ava Chen",
          "propertyOgTitle": "string",
          "propertyOgType": "string",
          "propertyOgUrl": "https://example.com",
          "relAppletouchiconprecomposed": "string",
          "relCanonical": "string",
          "relIcon": "string",
          "relStylesheet": "string",
          "robots": 1,
          "schemaJobpostingCount": 1,
          "title": "string",
          "titleClean": "string",
          "tld": "string",
          "tldcountry": "string",
          "url": "https://example.com"
        }
      },
      "product": "string",
      "status": "string",
      "texts": {
        "allArticle": "string",
        "allArticleSum": "string",
        "allContentSum": "string",
        "allIntroduction": "string",
        "allMetaarticle": "string",
        "allMetaarticleSum": "string",
        "homeArticle": "string",
        "homeArticleSum": "string",
        "homeCompany": "string",
        "homeContentSum": "string",
        "homeIntroduction": "string",
        "homeMetaarticle": "string",
        "homeMetaarticleSum": "string",
        "profilesAllKeyword": [
          "string"
        ],
        "profilesCity": "string",
        "profilesDescriptions": [
          "string"
        ],
        "profilesEmployees": 1,
        "profilesFacebookIndustry": "string",
        "profilesFacebookLikes": 1,
        "profilesFoundedYear": 1,
        "profilesFunctions": [
          "string"
        ],
        "profilesKeywords": [
          "string"
        ],
        "profilesLinkedinEmployees": "https://example.com",
        "profilesLinkedinEmployeesRange": "https://example.com",
        "profilesLinkedinFollowers": 1,
        "profilesLinkedinIndustries": "https://example.com",
        "profilesLinkedinIndustry": "https://example.com",
        "profilesLinkedinLocation": "https://example.com",
        "profilesLinkedinname": [
          "https://example.com"
        ],
        "profilesNaceIndustries": "string",
        "profilesName": "Ava Chen",
        "profilesRevenue": 1,
        "profilesReviews": 1,
        "socialDetail": [
          "string"
        ]
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
| `creditsUsed` | number |  |
| `creditsUsedMonth` | number |  |
| `domain` | string |  |
| `monthlyCredits` | number |  |
| `pages.all.article` | string |  |
| `pages.all.articleSum` | string |  |
| `pages.all.contentall` | string |  |
| `pages.all.contentSum` | string |  |
| `pages.all.introduction` | string |  |
| `pages.all.metaarticle` | string |  |
| `pages.all.metaarticleSum` | string |  |
| `pages.all.title` | string |  |
| `pages.home.alt[]` | string |  |
| `pages.home.article` | string |  |
| `pages.home.articledigest` | string |  |
| `pages.home.articledivCount` | number |  |
| `pages.home.articleFoot` | string |  |
| `pages.home.articleFootNormal` | number |  |
| `pages.home.articleHead` | string |  |
| `pages.home.articleimageCount` | number |  |
| `pages.home.articlelength` | number |  |
| `pages.home.articlelengthOrg` | number |  |
| `pages.home.articlelinesCount` | number |  |
| `pages.home.articlelineslong` | number |  |
| `pages.home.articlestart[]` | string |  |
| `pages.home.articleSum` | string |  |
| `pages.home.base` | string |  |
| `pages.home.bodyBase` | string |  |
| `pages.home.bodyDomain` | string |  |
| `pages.home.bodyHost` | string |  |
| `pages.home.bodylength` | number |  |
| `pages.home.bodyUrl` | string |  |
| `pages.home.cacheFile` | string |  |
| `pages.home.cleanArticle` | string |  |
| `pages.home.content` | string |  |
| `pages.home.contentall` | string |  |
| `pages.home.contentallSum` | string |  |
| `pages.home.contentdigest` | string |  |
| `pages.home.contentlength` | number |  |
| `pages.home.contentnoboiler` | string |  |
| `pages.home.contentSum` | string |  |
| `pages.home.domain` | string |  |
| `pages.home.firstText` | string |  |
| `pages.home.footer` | string |  |
| `pages.home.formcount` | number |  |
| `pages.home.frameraw[]` | string |  |
| `pages.home.fromCache` | number |  |
| `pages.home.h1[]` | string |  |
| `pages.home.head` | string |  |
| `pages.home.headLang` | string |  |
| `pages.home.headlength` | number |  |
| `pages.home.headsplit` | string |  |
| `pages.home.headsplitStart` | string |  |
| `pages.home.homepageHtml` | string |  |
| `pages.home.host` | string |  |
| `pages.home.htmlArticleSection` | number |  |
| `pages.home.htmlHeaderSection` | number |  |
| `pages.home.httpCode` | number |  |
| `pages.home.httpEquivXUaCompatible` | string |  |
| `pages.home.iframescount` | number |  |
| `pages.home.imagescount` | number |  |
| `pages.home.internallinksactive` | number |  |
| `pages.home.introduction` | string |  |
| `pages.home.introductiondigest` | string |  |
| `pages.home.l` | number |  |
| `pages.home.lang` | string |  |
| `pages.home.linkArticleEnd` | number |  |
| `pages.home.linkArticleEndInternal` | number |  |
| `pages.home.linkArticleStart` | number |  |
| `pages.home.linkArticleStartInternal` | number |  |
| `pages.home.linkContentEnd` | number |  |
| `pages.home.linkContentEndInternal` | number |  |
| `pages.home.linkContentStart` | number |  |
| `pages.home.linkContentStartInternal` | number |  |
| `pages.home.linkCount` | number |  |
| `pages.home.linkdomain[]` | string |  |
| `pages.home.linkraw[]` | string |  |
| `pages.home.linksactive` | number |  |
| `pages.home.linksanchor[]` | string |  |
| `pages.home.linksinarticleCount` | number |  |
| `pages.home.linksnofollow[]` | number |  |
| `pages.home.linkstitle[]` | string |  |
| `pages.home.logoAlt` | string |  |
| `pages.home.logoSrc` | string |  |
| `pages.home.metaarticle` | string |  |
| `pages.home.metaarticleRaw` | string |  |
| `pages.home.metaarticleSum` | string |  |
| `pages.home.metaCharset` | string |  |
| `pages.home.metaEncoding` | string |  |
| `pages.home.metaMsapplicationSquare150x150logo` | string |  |
| `pages.home.metaMsapplicationSquare310x310logo` | string |  |
| `pages.home.metaMsapplicationSquare70x70logo` | string |  |
| `pages.home.metaMsapplicationTilecolor` | string |  |
| `pages.home.metaMsapplicationWide310x150logo` | string |  |
| `pages.home.metaViewport` | string |  |
| `pages.home.outlinks` | number |  |
| `pages.home.pagetitle` | string |  |
| `pages.home.pagetitleMatch` | string |  |
| `pages.home.path` | string |  |
| `pages.home.pathClean` | string |  |
| `pages.home.pathqueryClean` | string |  |
| `pages.home.propertyOgSiteName` | string |  |
| `pages.home.propertyOgTitle` | string |  |
| `pages.home.propertyOgType` | string |  |
| `pages.home.propertyOgUrl` | string |  |
| `pages.home.relAppletouchiconprecomposed` | string |  |
| `pages.home.relCanonical` | string |  |
| `pages.home.relIcon` | string |  |
| `pages.home.relStylesheet` | string |  |
| `pages.home.robots` | number |  |
| `pages.home.schemaJobpostingCount` | number |  |
| `pages.home.title` | string |  |
| `pages.home.titleClean` | string |  |
| `pages.home.tld` | string |  |
| `pages.home.tldcountry` | string |  |
| `pages.home.url` | string |  |
| `product` | string |  |
| `status` | string |  |
| `texts.allArticle` | string |  |
| `texts.allArticleSum` | string |  |
| `texts.allContentSum` | string |  |
| `texts.allIntroduction` | string |  |
| `texts.allMetaarticle` | string |  |
| `texts.allMetaarticleSum` | string |  |
| `texts.homeArticle` | string |  |
| `texts.homeArticleSum` | string |  |
| `texts.homeCompany` | string |  |
| `texts.homeContentSum` | string |  |
| `texts.homeIntroduction` | string |  |
| `texts.homeMetaarticle` | string |  |
| `texts.homeMetaarticleSum` | string |  |
| `texts.profilesAllKeyword[]` | string |  |
| `texts.profilesCity` | string |  |
| `texts.profilesDescriptions[]` | string |  |
| `texts.profilesEmployees` | number |  |
| `texts.profilesFacebookIndustry` | string |  |
| `texts.profilesFacebookLikes` | number |  |
| `texts.profilesFoundedYear` | number |  |
| `texts.profilesFunctions[]` | string |  |
| `texts.profilesKeywords[]` | string |  |
| `texts.profilesLinkedinEmployees` | string |  |
| `texts.profilesLinkedinEmployeesRange` | string |  |
| `texts.profilesLinkedinFollowers` | number |  |
| `texts.profilesLinkedinIndustries` | string |  |
| `texts.profilesLinkedinIndustry` | string |  |
| `texts.profilesLinkedinLocation` | string |  |
| `texts.profilesLinkedinname[]` | string |  |
| `texts.profilesNaceIndustries` | string |  |
| `texts.profilesName` | string |  |
| `texts.profilesRevenue` | number |  |
| `texts.profilesReviews` | number |  |
| `texts.socialDetail[]` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Bedrijfsdata.nl API, this operation is `GET /rag_domain` (base URL `https://fapi.bedrijfsdata.nl/v1.2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/lookup-company-by-domain.md) for the provider-specific parameters and requirements.

