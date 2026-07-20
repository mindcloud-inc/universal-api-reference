# TPSCheck: Check phone number



```
GET https://connect.mindcloud.co/v1/universal/tPSCheck/latest/actions/check-phone-number
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TPSCheck `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tPSCheck/latest/actions/check-phone-number?connectionId=$CONNECTION_ID&phone=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "phone": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tPSCheck/latest/actions/check-phone-number?${params}`, {
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
| `phone` | string | yes | The UK phone number to verify. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ctps": true,
      "e164": "string",
      "input": "string",
      "line": {
        "country": "string",
        "location": "string",
        "originalCarrier": "string",
        "prefix": "string",
        "type": "string"
      },
      "reachability": {
        "confidence": "string",
        "status": "string"
      },
      "tps": true,
      "valid": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ctps` | boolean | Whether the number is registered with CTPS. |
| `e164` | string | E.164 formatted phone number. |
| `input` | string | The phone number as submitted. |
| `line` | object | Line metadata for the phone number. |
| `line.country` | string | Country associated with the number. |
| `line.location` | string | Geographic location associated with the number. |
| `line.originalCarrier` | string | Original carrier reported by TPSCheck. |
| `line.prefix` | string | Number prefix. |
| `line.type` | string | Detected line type. |
| `reachability` | object | Reachability metadata for the phone number. |
| `reachability.confidence` | string | Confidence of the reachability assessment. |
| `reachability.status` | string | Reachability status. |
| `tps` | boolean | Whether the number is registered with TPS. |
| `valid` | boolean | Whether the phone number is valid. |

## Native endpoint

Through the native TPSCheck API, this operation is `POST /check` (base URL `https://api.tpscheck.uk`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-phone-number.md) for the provider-specific parameters and requirements.

