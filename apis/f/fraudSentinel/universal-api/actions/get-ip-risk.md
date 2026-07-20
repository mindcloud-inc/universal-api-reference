# FraudSentinel: Get IP Risk



```
GET https://connect.mindcloud.co/v1/universal/fraudSentinel/latest/actions/get-ip-risk
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FraudSentinel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fraudSentinel/latest/actions/get-ip-risk?connectionId=$CONNECTION_ID&ip=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ip": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fraudSentinel/latest/actions/get-ip-risk?${params}`, {
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
| `ip` | string | yes | IP address to evaluate for fraud risk. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "flag": "string",
      "geo": "string",
      "ip": "string",
      "timestamp": 1,
      "userAgent": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `flag` | string |  |
| `geo` | string |  |
| `ip` | string |  |
| `timestamp` | number |  |
| `userAgent` | string |  |

## Native endpoint

Through the native FraudSentinel API, this operation is `POST /api/sentinel.json` (base URL `https://api.clickfreeze.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-ip-risk.md) for the provider-specific parameters and requirements.

