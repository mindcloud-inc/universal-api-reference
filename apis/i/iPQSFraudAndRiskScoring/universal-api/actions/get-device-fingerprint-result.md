# IPQS Fraud and Risk Scoring: Get Device Fingerprint Result

Retrieves device fingerprint verification results from IPQS.

```
GET https://connect.mindcloud.co/v1/universal/iPQSFraudAndRiskScoring/latest/actions/get-device-fingerprint-result
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a IPQS Fraud and Risk Scoring `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iPQSFraudAndRiskScoring/latest/actions/get-device-fingerprint-result?connectionId=$CONNECTION_ID&ip=string&deviceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ip": "string",
  "deviceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iPQSFraudAndRiskScoring/latest/actions/get-device-fingerprint-result?${params}`, {
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
| `ip` | string | yes | End-user IP address associated with the device ID. |
| `deviceId` | string | yes | Device fingerprint ID returned by the IPQS tracker. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native IPQS Fraud and Risk Scoring API returns.

## Native endpoint

Through the native IPQS Fraud and Risk Scoring API, this operation is `GET https://www.ipqualityscore.com/api/tracker/results/{{credentials.apiKey}}/:ip/:deviceId` (base URL `https://www.ipqualityscore.com/api/json`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-device-fingerprint-result.md) for the provider-specific parameters and requirements.

