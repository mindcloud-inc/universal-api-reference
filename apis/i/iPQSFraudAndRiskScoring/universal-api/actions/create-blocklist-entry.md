# IPQS Fraud and Risk Scoring: Create Blocklist Entry

Creates a new blocklist entry in IPQS.

```
POST https://connect.mindcloud.co/v1/universal/iPQSFraudAndRiskScoring/latest/actions/create-blocklist-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a IPQS Fraud and Risk Scoring `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/iPQSFraudAndRiskScoring/latest/actions/create-blocklist-entry" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "value": "8.8.8.8"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/iPQSFraudAndRiskScoring/latest/actions/create-blocklist-entry', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "value": "8.8.8.8"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `value` | string | yes | Value to add to the blocklist. Default: `8.8.8.8`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `reason` | string | no | Reason for adding the blocklist entry. Default: `MindCloud safe Stage 3 runtime test`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native IPQS Fraud and Risk Scoring API returns.

## Native endpoint

Through the native IPQS Fraud and Risk Scoring API, this operation is `POST /blocklist/create/{{credentials.apiKey}}` (base URL `https://www.ipqualityscore.com/api/json`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-blocklist-entry.md) for the provider-specific parameters and requirements.

