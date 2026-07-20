# Veriphone: Validate Phone Number



```
GET https://connect.mindcloud.co/v1/universal/veriphone/latest/actions/validate-phone-number
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Veriphone `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/veriphone/latest/actions/validate-phone-number?connectionId=$CONNECTION_ID&phone=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "phone": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/veriphone/latest/actions/validate-phone-number?${params}`, {
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
| `phone` | string | yes | Phone number to validate |
| `defaultCountry` | string | no | Default country code Example: `US`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "carrier": "string",
      "country": "string",
      "country_code": "string",
      "country_prefix": 1,
      "e164": "string",
      "international_number": "string",
      "local_number": "string",
      "phone": "string",
      "phone_region": "string",
      "phone_type": "string",
      "phone_valid": true,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `carrier` | string |  |
| `country` | string |  |
| `country_code` | string |  |
| `country_prefix` | number |  |
| `e164` | string |  |
| `international_number` | string |  |
| `local_number` | string |  |
| `phone` | string |  |
| `phone_region` | string |  |
| `phone_type` | string |  |
| `phone_valid` | boolean |  |
| `status` | string |  |

## Native endpoint

Through the native Veriphone API, this operation is `GET /v2/verify` (base URL `https://api.veriphone.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-phone-number.md) for the provider-specific parameters and requirements.

