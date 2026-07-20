# Tomba: Phone Validator

Validates a phone number in Tomba.

```
GET https://connect.mindcloud.co/v1/universal/tomba/latest/actions/phone-validator
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tomba `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tomba/latest/actions/phone-validator?connectionId=$CONNECTION_ID&phone=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "phone": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tomba/latest/actions/phone-validator?${params}`, {
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
| `phone` | string | yes |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `countryCode` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "carrier": "string",
      "country_code": "string",
      "e164_format": "string",
      "intl_format": "string",
      "line_type": "string",
      "valid": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `carrier` | string |  |
| `country_code` | string |  |
| `e164_format` | string |  |
| `intl_format` | string |  |
| `line_type` | string |  |
| `valid` | boolean |  |

## Native endpoint

Through the native Tomba API, this operation is `GET /phone-validator` (base URL `https://api.tomba.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/phone-validator.md) for the provider-specific parameters and requirements.

