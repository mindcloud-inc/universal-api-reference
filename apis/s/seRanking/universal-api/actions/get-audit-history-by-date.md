# SE Ranking Data: Get audit history by date

Retrieves audit history by date from SE Ranking Data.

```
GET https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/get-audit-history-by-date
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SE Ranking Data `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/get-audit-history-by-date?connectionId=$CONNECTION_ID&auditId=1&date=2026-01-01" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "auditId": "1",
  "date": "2026-01-01"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/get-audit-history-by-date?${params}`, {
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
| `date` | string | yes | Date for history retrieval (YYYY-MM-DD). Example: `2026-01-01`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "auditTime": "string",
      "domainData": {
        "allChecked": true,
        "backlinks": "https://example.com",
        "domain": "string",
        "domains": "string",
        "dt": 1,
        "expdate": "string",
        "indexGoogle": "string",
        "updated": "string"
      },
      "pagesData": {
        "blockedByNofollow": 1,
        "blockedByNoindex": 1,
        "cssNotMin": 1,
        "descriptionDuplicate": 1,
        "descriptionLong": 1,
        "descriptionMissing": 1,
        "extlinks3xx": 1,
        "extlinks4xx": 1,
        "extlinksNoAnchor": 1,
        "extlinksNofollow": 1,
        "extlinksTimeout": 1,
        "h1Duplicate": 1,
        "h1Long": 1,
        "h1Multiple": 1,
        "hreflangMultiple": 1,
        "hreflangNonCanonical": 1,
        "hreflangReturn": 1,
        "http4xx": 1,
        "imageBig": 1,
        "imageNoAlt": 1,
        "images4xx": 1,
        "jsMany": 1,
        "jsNotCached": 1,
        "jsNotMin": 1,
        "lessInlink": 1,
        "links3xx": 1,
        "linksNoAnchor": 1,
        "linksNofollow": 1,
        "redirect3xx": 1,
        "sameTitleH1": 1,
        "titleDuplicate": 1,
        "titleLong": 1,
        "titleShort": 1
      },
      "settings": {
        "allow": "string",
        "checkRobots": 1,
        "csr": 1,
        "csrDelay": 1,
        "customParams": "string",
        "disableAudit": 1,
        "disabledIssues": [
          "string"
        ],
        "disallow": "string",
        "disallowExt": "string",
        "hide": "string",
        "ignoreNofollow": 1,
        "ignoreNoindex": 1,
        "ignoreParams": 1,
        "login": "string",
        "maxDepth": 1,
        "maxDescriptionLen": 1,
        "maxH1Len": 1,
        "maxH2Len": 1,
        "maxPages": 1,
        "maxRedirects": 1,
        "maxReq": 1,
        "maxSize": 1,
        "maxTitleLen": 1,
        "minDescriptionLen": 1,
        "minTitleLen": 1,
        "minWords": 1,
        "password": "string",
        "reportEmail": "ava@example.com",
        "reportEmails": "ava@example.com",
        "scheduleDay": 1,
        "scheduleHour": 1,
        "scheduleRepeat": 1,
        "scheduleRepeatInterval": 1,
        "scheduleType": "string",
        "scheduleWday": 1,
        "scheduleWdays": [
          "string"
        ],
        "sendReport": 1,
        "sourceFile": 1,
        "sourceSite": 1,
        "sourceSitemap": 1,
        "sourceSubdomain": 1,
        "userAgent": 1
      },
      "totals": {
        "totalErrors": 1,
        "totalPages": 1,
        "totalPassed": 1,
        "totalWarnings": 1
      },
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `auditTime` | string |  |
| `domainData` | object |  |
| `domainData.allChecked` | boolean |  |
| `domainData.backlinks` | string |  |
| `domainData.domain` | string |  |
| `domainData.domains` | string |  |
| `domainData.dt` | number |  |
| `domainData.expdate` | string |  |
| `domainData.indexGoogle` | string |  |
| `domainData.updated` | string |  |
| `pagesData` | object |  |
| `pagesData.blockedByNofollow` | number |  |
| `pagesData.blockedByNoindex` | number |  |
| `pagesData.cssNotMin` | number |  |
| `pagesData.descriptionDuplicate` | number |  |
| `pagesData.descriptionLong` | number |  |
| `pagesData.descriptionMissing` | number |  |
| `pagesData.extlinks3xx` | number |  |
| `pagesData.extlinks4xx` | number |  |
| `pagesData.extlinksNoAnchor` | number |  |
| `pagesData.extlinksNofollow` | number |  |
| `pagesData.extlinksTimeout` | number |  |
| `pagesData.h1Duplicate` | number |  |
| `pagesData.h1Long` | number |  |
| `pagesData.h1Multiple` | number |  |
| `pagesData.hreflangMultiple` | number |  |
| `pagesData.hreflangNonCanonical` | number |  |
| `pagesData.hreflangReturn` | number |  |
| `pagesData.http4xx` | number |  |
| `pagesData.imageBig` | number |  |
| `pagesData.imageNoAlt` | number |  |
| `pagesData.images4xx` | number |  |
| `pagesData.jsMany` | number |  |
| `pagesData.jsNotCached` | number |  |
| `pagesData.jsNotMin` | number |  |
| `pagesData.lessInlink` | number |  |
| `pagesData.links3xx` | number |  |
| `pagesData.linksNoAnchor` | number |  |
| `pagesData.linksNofollow` | number |  |
| `pagesData.redirect3xx` | number |  |
| `pagesData.sameTitleH1` | number |  |
| `pagesData.titleDuplicate` | number |  |
| `pagesData.titleLong` | number |  |
| `pagesData.titleShort` | number |  |
| `settings` | object |  |
| `settings.allow` | string |  |
| `settings.checkRobots` | number |  |
| `settings.csr` | number |  |
| `settings.csrDelay` | number |  |
| `settings.customParams` | string |  |
| `settings.disableAudit` | number |  |
| `settings.disabledIssues` | array<string> |  |
| `settings.disallow` | string |  |
| `settings.disallowExt` | string |  |
| `settings.hide` | string |  |
| `settings.ignoreNofollow` | number |  |
| `settings.ignoreNoindex` | number |  |
| `settings.ignoreParams` | number |  |
| `settings.login` | string |  |
| `settings.maxDepth` | number |  |
| `settings.maxDescriptionLen` | number |  |
| `settings.maxH1Len` | number |  |
| `settings.maxH2Len` | number |  |
| `settings.maxPages` | number |  |
| `settings.maxRedirects` | number |  |
| `settings.maxReq` | number |  |
| `settings.maxSize` | number |  |
| `settings.maxTitleLen` | number |  |
| `settings.minDescriptionLen` | number |  |
| `settings.minTitleLen` | number |  |
| `settings.minWords` | number |  |
| `settings.password` | string |  |
| `settings.reportEmail` | string |  |
| `settings.reportEmails` | string |  |
| `settings.scheduleDay` | number |  |
| `settings.scheduleHour` | number |  |
| `settings.scheduleRepeat` | number |  |
| `settings.scheduleRepeatInterval` | number |  |
| `settings.scheduleType` | string |  |
| `settings.scheduleWday` | number |  |
| `settings.scheduleWdays` | array<string> |  |
| `settings.sendReport` | number |  |
| `settings.sourceFile` | number |  |
| `settings.sourceSite` | number |  |
| `settings.sourceSitemap` | number |  |
| `settings.sourceSubdomain` | number |  |
| `settings.userAgent` | number |  |
| `totals` | object |  |
| `totals.totalErrors` | number |  |
| `totals.totalPages` | number |  |
| `totals.totalPassed` | number |  |
| `totals.totalWarnings` | number |  |
| `version` | string |  |

## Native endpoint

Through the native SE Ranking Data API, this operation is `GET /site-audit/audits/history` (base URL `https://api.seranking.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-audit-history-by-date.md) for the provider-specific parameters and requirements.

