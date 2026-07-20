# IPQS Fraud and Risk Scoring: Delete Blocklist Entry

Deletes an existing blocklist entry from IPQS.

```
DELETE https://connect.mindcloud.co/v1/universal/iPQSFraudAndRiskScoring/latest/actions/delete-blocklist-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a IPQS Fraud and Risk Scoring `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/iPQSFraudAndRiskScoring/latest/actions/delete-blocklist-entry?connectionId=$CONNECTION_ID&value=8.8.8.8" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "value": "8.8.8.8"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iPQSFraudAndRiskScoring/latest/actions/delete-blocklist-entry?${params}`, {
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
| `value` | string | yes | Value to remove from the blocklist. Default: `8.8.8.8`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native IPQS Fraud and Risk Scoring API returns.

## Native endpoint

Through the native IPQS Fraud and Risk Scoring API, this operation is `POST /blocklist/delete/{{credentials.apiKey}}` (base URL `https://www.ipqualityscore.com/api/json`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-blocklist-entry.md) for the provider-specific parameters and requirements.

