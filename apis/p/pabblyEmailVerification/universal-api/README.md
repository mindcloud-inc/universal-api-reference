# <img src="https://images.mindcloud.co/apps/icons/captura-de-tela-2026-04-20-as-14_1776704753392.png" alt="Pabbly Email Verification logo" width="28" height="28"> Pabbly Email Verification: Universal API

Verify email addresses and inspect deliverability signals

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/pabblyEmailVerification/latest
- **Category:** Marketing
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.pabbly.com/email-list-cleaning/
- **Vendor API docs:** https://apidocs.pabbly.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Verify Single Email](actions/verify-single-email.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pabblyEmailVerification/latest/actions/verify-single-email?connectionId=$CONNECTION_ID&email=johnfabric%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Email Verification

| Action | Method | Description |
| --- | --- | --- |
| [Verify Single Email](actions/verify-single-email.md) | GET |  |

