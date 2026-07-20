# Abstract VAT Validator: Calculate VAT

Calculates VAT-compliant pricing for a country in Abstract VAT Validator.

```
GET https://connect.mindcloud.co/v1/universal/abstractVATValidator/latest/actions/calculate-vat
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Abstract VAT Validator `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/abstractVATValidator/latest/actions/calculate-vat?connectionId=$CONNECTION_ID&amount=175&country_code=DE" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "amount": "175",
  "country_code": "DE"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/abstractVATValidator/latest/actions/calculate-vat?${params}`, {
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
| `amount` | number | yes | The amount to calculate VAT for or from. Example: `175`. |
| `country_code` | string | yes | Two-letter ISO 3166-1 alpha-2 country code for the transaction. Example: `DE`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `is_vat_incl` | boolean | no | Set true when the amount already includes VAT and the API should split VAT out. |
| `vat_category` | string | no | Optional reduced-rate goods category to apply when supported for the country. Example: `standard`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount_excluding_vat": "string",
      "amount_including_vat": "string",
      "country": {
        "code": "string",
        "name": "Ava Chen"
      },
      "vat_amount": "string",
      "vat_category": "string",
      "vat_rate": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount_excluding_vat` | string | Amount excluding VAT returned by the calculation. |
| `amount_including_vat` | string | Amount including VAT returned by the calculation. |
| `country.code` | string | Two-letter country code used for the calculation. |
| `country.name` | string | Country name used for the calculation. |
| `vat_amount` | string | Calculated VAT amount. |
| `vat_category` | string | VAT category used for the calculation. |
| `vat_rate` | string | VAT rate used for the calculation. |

## Native endpoint

Through the native Abstract VAT Validator API, this operation is `GET /calculate` (base URL `https://vat.abstractapi.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/calculate-vat.md) for the provider-specific parameters and requirements.

