# IPQS Fraud and Risk Scoring: Get Device Fingerprint Stats

Retrieves device fingerprint statistics from IPQS.

```
GET https://connect.mindcloud.co/v1/universal/iPQSFraudAndRiskScoring/latest/actions/get-device-fingerprint-stats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a IPQS Fraud and Risk Scoring `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iPQSFraudAndRiskScoring/latest/actions/get-device-fingerprint-stats?connectionId=$CONNECTION_ID&key=string&secret=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "key": "string",
  "secret": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iPQSFraudAndRiskScoring/latest/actions/get-device-fingerprint-stats?${params}`, {
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
| `key` | string | yes | Site domain or domain that requested the custom integration. |
| `secret` | string | yes | User secret created during the IPQS custom integration authentication process. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `domain` | string | no | Optional domain to fetch trackers for. |
| `start` | date | no | Optional start date in YYYY-MM-DD format. |
| `stop` | date | no | Optional stop date in YYYY-MM-DD format, no more than 90 days from start. |
| `trackerName` | string | no | Optional exact tracker name to fetch. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native IPQS Fraud and Risk Scoring API returns.

## Native endpoint

Through the native IPQS Fraud and Risk Scoring API, this operation is `POST /webhooks/ExampleIntegration/json/device_tracker_statistics` (base URL `https://www.ipqualityscore.com/api/json`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-device-fingerprint-stats.md) for the provider-specific parameters and requirements.

