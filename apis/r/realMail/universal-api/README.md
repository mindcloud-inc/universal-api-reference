# <img src="https://images.mindcloud.co/apps/icons/captura-de-tela-2026-04-08-as-09_1775651547816.png" alt="RealMail logo" width="28" height="28"> RealMail: Universal API

Validate email addresses with RealMail using their official verification API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/realMail/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.realmail.dev
- **Vendor API docs:** https://www.realmail.dev/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Validate Email](actions/validate-email.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/realMail/latest/actions/validate-email?connectionId=$CONNECTION_ID&email=email%40domain.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Emails

| Action | Method | Description |
| --- | --- | --- |
| [Validate Email](actions/validate-email.md) | GET | Validates an email address with RealMail. |

