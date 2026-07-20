# Veriphone: Get Example Phone Number



```
GET https://connect.mindcloud.co/v1/universal/veriphone/latest/actions/get-example-phone-number
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Veriphone `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/veriphone/latest/actions/get-example-phone-number?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/veriphone/latest/actions/get-example-phone-number?${params}`, {
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
| `type` | string | no | Example number type Default: `mobile`. |
| `countryCode` | string | no | Country code Example: `US`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "country_code": "string",
      "country_prefix": 1,
      "e164": "string",
      "international_number": "string",
      "local_number": "string",
      "phone_type": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `country_code` | string | ISO 3166-1 alpha-2 country code. |
| `country_prefix` | number | Country calling prefix. |
| `e164` | string | E.164 formatted phone number. |
| `international_number` | string | Formatted international number. |
| `local_number` | string | Formatted local number. |
| `phone_type` | string | Example phone type returned by Veriphone. |
| `status` | string | Success state for the helper response. |

## Native endpoint

Through the native Veriphone API, this operation is `GET /v2/example` (base URL `https://api.veriphone.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-example-phone-number.md) for the provider-specific parameters and requirements.

