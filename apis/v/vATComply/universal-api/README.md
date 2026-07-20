# <img src="https://images.mindcloud.co/apps/icons/v-atcomply_1777039091777.png" alt="VAT Comply logo" width="28" height="28"> VAT Comply: Universal API

Validate VAT numbers and IBANs, and fetch VAT and FX rates

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/vATComply/latest
- **Category:** Commerce / Accounting
- **Actions:** 10
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.vatcomply.com
- **Vendor API docs:** https://www.vatcomply.com

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Check API Health](actions/check-api-health.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vATComply/latest/actions/check-api-health?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (10)

### Api Information

| Action | Method | Description |
| --- | --- | --- |
| [Get API Information](actions/get-api-information.md) | GET | Retrieves API information from VAT Comply. |

### Country

| Action | Method | Description |
| --- | --- | --- |
| [List Countries](actions/list-countries.md) | GET | Retrieves a list of countries from VAT Comply. |

### Currency

| Action | Method | Description |
| --- | --- | --- |
| [List Currencies](actions/list-currencies.md) | GET | Retrieves supported currencies from VAT Comply. |

### Exchange Rates

| Action | Method | Description |
| --- | --- | --- |
| [Get Exchange Rates](actions/get-exchange-rates.md) | GET | Retrieves exchange rates from VAT Comply. |

### Geolocation

| Action | Method | Description |
| --- | --- | --- |
| [Geolocate Request IP](actions/geolocate-request-ip.md) | GET | Retrieves request IP geolocation from VAT Comply. |

### Health Status

| Action | Method | Description |
| --- | --- | --- |
| [Check API Health](actions/check-api-health.md) | GET | Retrieves API health status from VAT Comply. |

### Iban Validation

| Action | Method | Description |
| --- | --- | --- |
| [Validate IBAN](actions/validate-iban.md) | GET | Validates an IBAN in VAT Comply. |

### Readiness Status

| Action | Method | Description |
| --- | --- | --- |
| [Check API Readiness](actions/check-api-readiness.md) | GET | Retrieves API readiness status from VAT Comply. |

### Vat Rate

| Action | Method | Description |
| --- | --- | --- |
| [List VAT Rates](actions/list-vat-rates.md) | GET | Retrieves VAT rates from VAT Comply. |

### Vat Validation

| Action | Method | Description |
| --- | --- | --- |
| [Validate VAT Number](actions/validate-vat-number.md) | GET | Validates a VAT number in VAT Comply. |

