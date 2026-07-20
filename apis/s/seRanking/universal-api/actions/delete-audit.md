# SE Ranking Data: Delete audit

Deletes an audit from SE Ranking Data.

```
DELETE https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/delete-audit
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SE Ranking Data `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/delete-audit?connectionId=$CONNECTION_ID&auditId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "auditId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/delete-audit?${params}`, {
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
      "value": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | array | The raw response body. The saved successful response was an empty array (HTTP 200). |

## Native endpoint

Through the native SE Ranking Data API, this operation is `DELETE /site-audit/audits` (base URL `https://api.seranking.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-audit.md) for the provider-specific parameters and requirements.

