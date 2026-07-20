# <img src="https://images.mindcloud.co/apps/icons/govuk-app-icon-0bca94cf05737106d8e80f32a66f773d7b6ff9b9652fc555917d855914309af0_1777930035058.png" alt="UK Check VAT logo" width="28" height="28"> UK Check VAT: Universal API

Check whether UK VAT registration numbers are valid, retrieve registered business details, and optionally generate an HMRC consultation reference for audit evidence.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/uKCheckVAT/latest
- **Category:** Commerce / Accounting
- **Actions:** 2
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://developer.service.hmrc.gov.uk/api-documentation/docs/api/service/vat-registered-companies-api/2.0
- **Vendor API docs:** https://developer.service.hmrc.gov.uk/api-documentation/docs/api/service/vat-registered-companies-api/2.0

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Check VAT Registration](actions/check-vat-registration.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uKCheckVAT/latest/actions/check-vat-registration?connectionId=$CONNECTION_ID&targetVrn=553557881" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (2)

### Vat Registered Company

| Action | Method | Description |
| --- | --- | --- |
| [Check VAT Registration](actions/check-vat-registration.md) | GET |  |
| [Check VAT Registration With Reference Number](actions/check-vat-registration-with-reference-number.md) | GET |  |

