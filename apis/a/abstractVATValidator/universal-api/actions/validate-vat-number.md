# Abstract VAT Validator: Validate VAT Number

Validates a VAT number and returns company details from Abstract VAT Validator.

```
GET https://connect.mindcloud.co/v1/universal/abstractVATValidator/latest/actions/validate-vat-number
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Abstract VAT Validator `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/abstractVATValidator/latest/actions/validate-vat-number?connectionId=$CONNECTION_ID&vat_number=SE556656688001" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "vat_number": "SE556656688001"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/abstractVATValidator/latest/actions/validate-vat-number?${params}`, {
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
| `vat_number` | string | yes | The VAT number to validate. Example: `SE556656688001`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "company": {
        "address": "string",
        "name": "Ava Chen"
      },
      "country": {
        "code": "string",
        "name": "Ava Chen"
      },
      "valid": true,
      "vat_number": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `company.address` | string | Registered company address returned for a valid VAT number. |
| `company.name` | string | Registered company name returned for a valid VAT number. |
| `country.code` | string | Two-letter country code returned for the VAT number. |
| `country.name` | string | Country name returned for the VAT number. |
| `valid` | boolean | Whether the submitted VAT number is valid. |
| `vat_number` | string | VAT number returned by the validation request. |

## Native endpoint

Through the native Abstract VAT Validator API, this operation is `GET /validate` (base URL `https://vat.abstractapi.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-vat-number.md) for the provider-specific parameters and requirements.

