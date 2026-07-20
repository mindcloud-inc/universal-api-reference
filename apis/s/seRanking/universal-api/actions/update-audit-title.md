# SE Ranking Data: Update audit title

Updates an audit title in SE Ranking Data.

```
PUT https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/update-audit-title
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SE Ranking Data `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/update-audit-title" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "auditId": "1",
  "title": "My Audit"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/seRanking/latest/actions/update-audit-title', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "auditId": "1",
    "title": "My Audit"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `auditId` | list<string> | yes | Audit identifier. Example: `1`. |
| `title` | string | yes | New audit title. Example: `My Audit`. |

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

Through the native SE Ranking Data API, this operation is `PATCH /site-audit/audits` (base URL `https://api.seranking.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-audit-title.md) for the provider-specific parameters and requirements.

