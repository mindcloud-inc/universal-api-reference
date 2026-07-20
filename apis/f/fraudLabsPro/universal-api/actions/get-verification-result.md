# FraudLabs Pro: Get Verification Result

Retrieves an SMS verification result from FraudLabs Pro.

```
GET https://connect.mindcloud.co/v1/universal/fraudLabsPro/latest/actions/get-verification-result
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FraudLabs Pro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fraudLabsPro/latest/actions/get-verification-result?connectionId=$CONNECTION_ID&tran_id=string&otp=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "tran_id": "string",
  "otp": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fraudLabsPro/latest/actions/get-verification-result?${params}`, {
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
| `tran_id` | string | yes | The transaction id returned by Send SMS Verification. |
| `otp` | string | yes | The one-time password received by the user. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | string |  |

## Native endpoint

Through the native FraudLabs Pro API, this operation is `GET v2/verification/result` (base URL `https://api.fraudlabspro.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-verification-result.md) for the provider-specific parameters and requirements.

