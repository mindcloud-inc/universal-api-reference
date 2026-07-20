# <img src="https://images.mindcloud.co/apps/icons/abstract-api-favicon_1777397261742.png" alt="Abstract IBAN Validator logo" width="28" height="28"> Abstract IBAN Validator: Universal API

Validate International Bank Account Numbers (IBANs) with Abstract's IBAN Validation API and return whether the submitted IBAN is valid.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/abstractIBANValidator/latest
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.abstractapi.com/api/iban-validation
- **Vendor API docs:** https://docs.abstractapi.com/api/iban-validation

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Validate IBAN](actions/validate-iban.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/abstractIBANValidator/latest/actions/validate-iban?connectionId=$CONNECTION_ID&iban=BE71096123456769" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Iban Validation Result

| Action | Method | Description |
| --- | --- | --- |
| [Validate IBAN](actions/validate-iban.md) | GET |  |

