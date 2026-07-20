# <img src="https://images.mindcloud.co/apps/icons/images_1775766219919.png" alt="API Labz logo" width="28" height="28"> API Labz: Universal API

API Labz gives agents a broad catalog of AI, search, validation, lookup, document, and business utility APIs over a single bearer-auth REST surface.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/aPILabz/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 5
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://apilabz.com
- **Vendor API docs:** https://apilabz.apidog.io/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Email Validator](actions/email-validator.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aPILabz/latest/actions/email-validator?connectionId=$CONNECTION_ID&emailAddress=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (5)

### Accounts

| Action | Method | Description |
| --- | --- | --- |
| [Domain Lookup](actions/domain-lookup.md) | GET | Retrieves domain information from API Labz. |
| [Domain WHOIS Lookup](actions/domain-whois-lookup.md) | GET | Retrieves WHOIS details for a domain in API Labz. |

### Bank Infos

| Action | Method | Description |
| --- | --- | --- |
| [IBAN Validator](actions/iban-validator.md) | GET | Validates an IBAN with API Labz. |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Email Validator](actions/email-validator.md) | GET | Validates an email address with API Labz. |

### Customers

| Action | Method | Description |
| --- | --- | --- |
| [VAT Validator](actions/vat-validator.md) | GET | Validates a VAT number with API Labz. |

