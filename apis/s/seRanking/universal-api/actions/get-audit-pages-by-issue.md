# SE Ranking Data: Get audit pages by issue

Retrieves audit pages by issue from SE Ranking Data.

```
GET https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/get-audit-pages-by-issue
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SE Ranking Data `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/get-audit-pages-by-issue?connectionId=$CONNECTION_ID&auditId=1&code=101" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "auditId": "1",
  "code": "101"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/get-audit-pages-by-issue?${params}`, {
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
| `code` | string | yes | Issue code filter. Example: `101`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "totalUrls": 1,
      "urls": [
        "https://example.com"
      ],
      "urlsType": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `totalUrls` | number |  |
| `urls` | array<string> |  |
| `urlsType` | string |  |

## Native endpoint

Through the native SE Ranking Data API, this operation is `GET /site-audit/audits/issue-pages` (base URL `https://api.seranking.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-audit-pages-by-issue.md) for the provider-specific parameters and requirements.

