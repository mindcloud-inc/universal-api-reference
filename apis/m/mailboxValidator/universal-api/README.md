# <img src="https://images.mindcloud.co/apps/icons/mailbox-validator_1775657980814.png" alt="MailboxValidator logo" width="28" height="28"> MailboxValidator: Universal API

Validate email addresses and detect disposable or free providers

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/mailboxValidator/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 3
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.mailboxvalidator.com/
- **Vendor API docs:** https://www.mailboxvalidator.com/web-service

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Check Free Email Provider](actions/check-free-email-provider.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailboxValidator/latest/actions/check-free-email-provider?connectionId=$CONNECTION_ID&email=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (3)

### Email Validation

| Action | Method | Description |
| --- | --- | --- |
| [Check Disposable Email](actions/check-disposable-email.md) | GET |  |
| [Check Free Email Provider](actions/check-free-email-provider.md) | GET |  |
| [Validate Email Address](actions/validate-email-address.md) | GET |  |

