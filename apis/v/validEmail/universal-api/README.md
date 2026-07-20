# <img src="https://images.mindcloud.co/apps/icons/valid-email_1776343146966.png" alt="ValidEmail logo" width="28" height="28"> ValidEmail: Universal API

Validate email addresses in real time with the ValidEmail API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/validEmail/latest
- **Category:** Communication / Email Communications
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.validemail.net
- **Vendor API docs:** https://www.validemail.net/Docs/api-python

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Verify Email](actions/verify-email.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/validEmail/latest/actions/verify-email?connectionId=$CONNECTION_ID&email=name%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Email Verification

| Action | Method | Description |
| --- | --- | --- |
| [Verify Email](actions/verify-email.md) | GET | Verifies an email address with ValidEmail. |

