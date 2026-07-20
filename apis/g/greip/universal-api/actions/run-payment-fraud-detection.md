# Greip - Fraud Prevention: Run Payment Fraud Detection

Runs payment fraud detection in Greip.

```
GET https://connect.mindcloud.co/v1/universal/greip/latest/actions/run-payment-fraud-detection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Greip - Fraud Prevention `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/greip/latest/actions/run-payment-fraud-detection?connectionId=$CONNECTION_ID&data=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "data": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/greip/latest/actions/run-payment-fraud-detection?${params}`, {
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
| `data` | object | yes | Structured payment-fraud input object documented by Greip for the scoring request body. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "custom_rules_applied": {},
      "rules": [
        {}
      ],
      "rulesChecked": 1,
      "rulesDetected": 1,
      "score": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `custom_rules_applied` | object |  |
| `rules` | array<object> |  |
| `rulesChecked` | number |  |
| `rulesDetected` | number |  |
| `score` | number |  |

## Native endpoint

Through the native Greip - Fraud Prevention API, this operation is `POST /scoring/payment` (base URL `https://greipapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/run-payment-fraud-detection.md) for the provider-specific parameters and requirements.

