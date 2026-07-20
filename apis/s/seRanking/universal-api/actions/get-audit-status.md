# SE Ranking Data: Get audit status

Retrieves audit status from SE Ranking Data.

```
GET https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/get-audit-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SE Ranking Data `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/get-audit-status?connectionId=$CONNECTION_ID&auditId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "auditId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/get-audit-status?${params}`, {
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
      "startTime": "string",
      "status": "string",
      "totalErrors": 1,
      "totalPages": 1,
      "totalPassed": 1,
      "totalWarnings": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `auditTime` | string |  |
| `startTime` | string |  |
| `status` | string |  |
| `totalErrors` | number |  |
| `totalPages` | number |  |
| `totalPassed` | number |  |
| `totalWarnings` | number |  |

## Native endpoint

Through the native SE Ranking Data API, this operation is `GET /site-audit/audits/status` (base URL `https://api.seranking.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-audit-status.md) for the provider-specific parameters and requirements.

