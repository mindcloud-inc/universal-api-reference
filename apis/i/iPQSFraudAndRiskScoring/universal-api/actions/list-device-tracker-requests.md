# IPQS Fraud and Risk Scoring: List Device Tracker Requests

Retrieves previous device fingerprint requests from IPQS.

```
GET https://connect.mindcloud.co/v1/universal/iPQSFraudAndRiskScoring/latest/actions/list-device-tracker-requests
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a IPQS Fraud and Risk Scoring `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iPQSFraudAndRiskScoring/latest/actions/list-device-tracker-requests?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iPQSFraudAndRiskScoring/latest/actions/list-device-tracker-requests?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native IPQS Fraud and Risk Scoring API returns.

## Native endpoint

Through the native IPQS Fraud and Risk Scoring API, this operation is `GET /requests/{{credentials.apiKey}}/list` (base URL `https://www.ipqualityscore.com/api/json`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-device-tracker-requests.md) for the provider-specific parameters and requirements.

