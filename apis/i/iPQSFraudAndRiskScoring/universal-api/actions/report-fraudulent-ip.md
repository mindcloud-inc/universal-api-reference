# IPQS Fraud and Risk Scoring: Report Fraudulent IP

Reports a fraudulent IP address to IPQS.

```
POST https://connect.mindcloud.co/v1/universal/iPQSFraudAndRiskScoring/latest/actions/report-fraudulent-ip
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a IPQS Fraud and Risk Scoring `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/iPQSFraudAndRiskScoring/latest/actions/report-fraudulent-ip" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "ip": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/iPQSFraudAndRiskScoring/latest/actions/report-fraudulent-ip', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "ip": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `ip` | string | yes | IPv4 or IPv6 address to report. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native IPQS Fraud and Risk Scoring API returns.

## Native endpoint

Through the native IPQS Fraud and Risk Scoring API, this operation is `GET /report/{{credentials.apiKey}}` (base URL `https://www.ipqualityscore.com/api/json`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/report-fraudulent-ip.md) for the provider-specific parameters and requirements.

