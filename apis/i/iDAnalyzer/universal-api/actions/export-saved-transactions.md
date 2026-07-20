# ID Analyzer: Export saved transactions

Creates a saved transaction export in ID Analyzer.

```
POST https://connect.mindcloud.co/v1/universal/iDAnalyzer/latest/actions/export-saved-transactions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ID Analyzer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/iDAnalyzer/latest/actions/export-saved-transactions" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "exportType": "json"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/iDAnalyzer/latest/actions/export-saved-transactions', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "exportType": "json"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `exportType` | string | yes | Export format: csv or json. Default: `json`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ID Analyzer API returns.

## Native endpoint

Through the native ID Analyzer API, this operation is `POST /export/transaction` (base URL `https://api2.idanalyzer.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/export-saved-transactions.md) for the provider-specific parameters and requirements.

