# Greip - Fraud Prevention: Get Phone Number Scoring

Retrieves phone number risk scoring from Greip.

```
GET https://connect.mindcloud.co/v1/universal/greip/latest/actions/get-phone-number-scoring
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Greip - Fraud Prevention `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/greip/latest/actions/get-phone-number-scoring?connectionId=$CONNECTION_ID&phone=string&countryCode=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "phone": "string",
  "countryCode": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/greip/latest/actions/get-phone-number-scoring?${params}`, {
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
| `phone` | string | yes | The phone number to validate. |
| `countryCode` | string | yes | The ISO 3166-1 alpha-2 country code for the phone number. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "carrier": "string",
      "custom_rules_applied": {},
      "isValid": true,
      "reason": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `carrier` | string |  |
| `custom_rules_applied` | object |  |
| `isValid` | boolean |  |
| `reason` | string |  |

## Native endpoint

Through the native Greip - Fraud Prevention API, this operation is `GET /scoring/phone` (base URL `https://greipapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-phone-number-scoring.md) for the provider-specific parameters and requirements.

