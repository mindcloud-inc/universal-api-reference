# <img src="https://images.mindcloud.co/apps/icons/abstract-api-favicon_1777397377492.png" alt="Abstract VAT Validator logo" width="28" height="28"> Abstract VAT Validator: Universal API

Validate VAT numbers, calculate VAT amounts, and retrieve VAT category rates using Abstract's VAT Validation API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/abstractVATValidator/latest
- **Category:** Commerce / Accounting
- **Actions:** 3
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.abstractapi.com/api/vat-validation-rates-api
- **Vendor API docs:** https://docs.abstractapi.com/api/vat-validation

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Validate VAT Number](actions/validate-vat-number.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/abstractVATValidator/latest/actions/validate-vat-number?connectionId=$CONNECTION_ID&vat_number=SE556656688001" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (3)

### Vat Calculation

| Action | Method | Description |
| --- | --- | --- |
| [Calculate VAT](actions/calculate-vat.md) | GET | Calculates VAT-compliant pricing for a country in Abstract VAT Validator. |

### Vat Category

| Action | Method | Description |
| --- | --- | --- |
| [Get VAT Categories](actions/get-vat-categories.md) | GET | Retrieves VAT rate categories for a country from Abstract VAT Validator. |

### Vat Registration

| Action | Method | Description |
| --- | --- | --- |
| [Validate VAT Number](actions/validate-vat-number.md) | GET | Validates a VAT number and returns company details from Abstract VAT Validator. |

