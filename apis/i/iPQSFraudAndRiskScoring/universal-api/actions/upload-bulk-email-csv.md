# IPQS Fraud and Risk Scoring: Upload Bulk Email CSV

Uploads a bulk email validation CSV to IPQS.

```
POST https://connect.mindcloud.co/v1/universal/iPQSFraudAndRiskScoring/latest/actions/upload-bulk-email-csv
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a IPQS Fraud and Risk Scoring `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/iPQSFraudAndRiskScoring/latest/actions/upload-bulk-email-csv" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "input[]": [
    [
      "support@ipqualityscore.com"
    ],
    [
      "test@example.com"
    ]
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/iPQSFraudAndRiskScoring/latest/actions/upload-bulk-email-csv', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "input[]": [["support@ipqualityscore.com"],["test@example.com"]]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `input[]` | array<array> | yes | Rows to upload for processing as JSON. Default: `[["support@ipqualityscore.com"],["test@example.com"]]`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fileName` | string | no | Optional name for the uploaded CSV. Default: `mindcloud-ipqs-email-sample.csv`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native IPQS Fraud and Risk Scoring API returns.

## Native endpoint

Through the native IPQS Fraud and Risk Scoring API, this operation is `POST /csv/upload` (base URL `https://www.ipqualityscore.com/api/json`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-bulk-email-csv.md) for the provider-specific parameters and requirements.

