# VatcheckAPI: Validate VAT Number

Validates a VAT number in VatcheckAPI.

```
GET https://connect.mindcloud.co/v1/universal/vatcheckAPI/latest/actions/validate-vat-number
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a VatcheckAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vatcheckAPI/latest/actions/validate-vat-number?connectionId=$CONNECTION_ID&vat_number=LU26375245" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "vat_number": "LU26375245"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vatcheckAPI/latest/actions/validate-vat-number?${params}`, {
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
| `vat_number` | string | yes | VAT number to query. It can include the country prefix, or be provided with Country Code. Example: `LU26375245`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `country_code` | string | no | ISO Alpha-2 country code for the VAT number, for example LU. Required only when the VAT number does not include its country prefix. Example: `LU`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "checksum_valid": true,
      "country_code": "string",
      "format_valid": true,
      "registration_info": {
        "address": "string",
        "address_parts": {},
        "checked_at": "2026-05-07T12:00:00.000Z",
        "is_registered": true,
        "name": "Ava Chen"
      },
      "registration_info_history": [
        {
          "address": "string",
          "checked_at": "2026-05-07T12:00:00.000Z",
          "created_at": "2026-05-07T12:00:00.000Z",
          "is_registered": true,
          "name": "Ava Chen"
        }
      ],
      "vat_number": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `checksum_valid` | boolean | Whether the VAT number checksum is valid. |
| `country_code` | string | ISO Alpha-2 country code for the VAT number. |
| `format_valid` | boolean | Whether the VAT number format is valid. |
| `registration_info` | object | Current registration details returned when available. |
| `registration_info_history` | array<object> | Historical registration information entries. |
| `registration_info_history[].address` | string | Registered company address for this history entry. |
| `registration_info_history[].checked_at` | date | Timestamp when this historical registration state was checked. |
| `registration_info_history[].created_at` | date | Timestamp when this historical entry was created. |
| `registration_info_history[].is_registered` | boolean | Whether the VAT number was registered for this history entry. |
| `registration_info_history[].name` | string | Registered company name for this history entry. |
| `registration_info.address` | string | Registered company address. |
| `registration_info.address_parts` | object | Structured address parts, when available. |
| `registration_info.checked_at` | date | Timestamp when the current registration data was checked. |
| `registration_info.is_registered` | boolean | Whether the VAT number is currently registered. |
| `registration_info.name` | string | Registered company name. |
| `vat_number` | string | VAT number returned by the validation endpoint. |

## Native endpoint

Through the native VatcheckAPI API, this operation is `GET /v2/check` (base URL `https://api.vatcheckapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-vat-number.md) for the provider-specific parameters and requirements.

