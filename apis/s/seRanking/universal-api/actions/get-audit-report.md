# SE Ranking Data: Get audit report

Retrieves an audit report from SE Ranking Data.

```
GET https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/get-audit-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SE Ranking Data `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/get-audit-report?connectionId=$CONNECTION_ID&auditId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "auditId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/get-audit-report?${params}`, {
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
      "auditTime": "string",
      "chromeux": [
        {
          "summary": "string"
        }
      ],
      "domainProps": {
        "allChecked": true,
        "backlinks": "https://example.com",
        "domain": "string",
        "domains": "string",
        "dt": 1,
        "expdate": "string",
        "indexBing": 1,
        "indexGoogle": "string",
        "indexYahoo": 1,
        "updated": "string"
      },
      "isFinished": true,
      "scorePercent": 1,
      "sections": [
        {
          "name": "Ava Chen",
          "props": {
            "code": "string",
            "name": "Ava Chen",
            "status": "string",
            "value": 1
          },
          "uid": "string"
        }
      ],
      "totalErrors": 1,
      "totalNotices": 1,
      "totalPages": 1,
      "totalPassed": 1,
      "totalWarnings": 1,
      "version": "string",
      "weightedScorePercent": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `auditTime` | string |  |
| `chromeux` | array<object> |  |
| `chromeux[].summary` | string |  |
| `domainProps` | object |  |
| `domainProps.allChecked` | boolean |  |
| `domainProps.backlinks` | string |  |
| `domainProps.domain` | string |  |
| `domainProps.domains` | string |  |
| `domainProps.dt` | number |  |
| `domainProps.expdate` | string |  |
| `domainProps.indexBing` | number |  |
| `domainProps.indexGoogle` | string |  |
| `domainProps.indexYahoo` | number |  |
| `domainProps.updated` | string |  |
| `isFinished` | boolean |  |
| `scorePercent` | number |  |
| `sections` | array<object> |  |
| `sections[].name` | string |  |
| `sections[].props.code` | string |  |
| `sections[].props.name` | string |  |
| `sections[].props.status` | string |  |
| `sections[].props.value` | number |  |
| `sections[].uid` | string |  |
| `totalErrors` | number |  |
| `totalNotices` | number |  |
| `totalPages` | number |  |
| `totalPassed` | number |  |
| `totalWarnings` | number |  |
| `version` | string |  |
| `weightedScorePercent` | number |  |

## Native endpoint

Through the native SE Ranking Data API, this operation is `GET /site-audit/audits/report` (base URL `https://api.seranking.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-audit-report.md) for the provider-specific parameters and requirements.

