# <img src="https://images.mindcloud.co/apps/icons/mightora-io-logo4-200x900-invert_1777484831858.png" alt="Email Domain Checker logo" width="28" height="28"> Email Domain Checker: Universal API

Check email domains for deliverability and validity

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/emailDomainChecker/latest
- **Category:** Communication / Email Communications
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://mightora.io/tools/power-automate-connectors/email-domain-checker/
- **Vendor API docs:** https://mightora.io/tools/power-automate-connectors/email-domain-checker/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Check Domain](actions/check-domain.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/emailDomainChecker/latest/actions/check-domain?connectionId=$CONNECTION_ID&domain=mightora.io" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Email Domain

| Action | Method | Description |
| --- | --- | --- |
| [Check Domain](actions/check-domain.md) | GET |  |

