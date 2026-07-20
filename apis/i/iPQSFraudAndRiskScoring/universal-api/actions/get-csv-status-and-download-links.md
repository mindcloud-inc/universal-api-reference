# IPQS Fraud and Risk Scoring: Get CSV Status And Download Links

Retrieves CSV processing status and download links from IPQS.

```
GET https://connect.mindcloud.co/v1/universal/iPQSFraudAndRiskScoring/latest/actions/get-csv-status-and-download-links
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a IPQS Fraud and Risk Scoring `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iPQSFraudAndRiskScoring/latest/actions/get-csv-status-and-download-links?connectionId=$CONNECTION_ID&csvId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "csvId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iPQSFraudAndRiskScoring/latest/actions/get-csv-status-and-download-links?${params}`, {
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
| `csvId` | number | yes | CSV ID returned by a prior upload. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native IPQS Fraud and Risk Scoring API returns.

## Native endpoint

Through the native IPQS Fraud and Risk Scoring API, this operation is `GET /csv/{{credentials.apiKey}}/status/:csvId` (base URL `https://www.ipqualityscore.com/api/json`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-csv-status-and-download-links.md) for the provider-specific parameters and requirements.

