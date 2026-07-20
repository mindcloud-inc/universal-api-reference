# <img src="https://images.mindcloud.co/apps/icons/mailer-send_1773868062551.png" alt="MailerSend logo" width="28" height="28"> MailerSend: Universal API

Transactional email and SMS platform for sending, tracking, and managing domains, identities, templates, recipients, and delivery events.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/mailerSend/latest
- **Category:** Communication / Email Communications
- **Actions:** 28
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.mailersend.com
- **Vendor API docs:** https://developers.mailersend.com/api/v1/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Messages](actions/list-messages.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailerSend/latest/actions/list-messages?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (28)

### Activity

| Action | Method | Description |
| --- | --- | --- |
| [Get Activity](actions/get-activity.md) | GET |  |
| [List Activity](actions/list-activity.md) | GET |  |

### Domain

| Action | Method | Description |
| --- | --- | --- |
| [Add Domain](actions/add-domain.md) | POST |  |
| [Delete Domain](actions/delete-domain.md) | DELETE |  |
| [Get Domain](actions/get-domain.md) | GET |  |
| [Get Domain DNS Records](actions/get-domain-dns-records.md) | GET |  |
| [Get Domain Verification Status](actions/get-domain-verification-status.md) | GET |  |
| [List Domains](actions/list-domains.md) | GET |  |

### Email

| Action | Method | Description |
| --- | --- | --- |
| [Get Bulk Email Status](actions/get-bulk-email-status.md) | GET |  |
| [Send Email](actions/send-email.md) | POST |  |

### Message

| Action | Method | Description |
| --- | --- | --- |
| [Get Message](actions/get-message.md) | GET |  |
| [List Messages](actions/list-messages.md) | GET |  |

### Metric

| Action | Method | Description |
| --- | --- | --- |
| [Get Analytics By Country](actions/get-analytics-by-country.md) | GET |  |
| [Get Analytics By Date](actions/get-analytics-by-date.md) | GET |  |

### Recipient

| Action | Method | Description |
| --- | --- | --- |
| [Get Recipient](actions/get-recipient.md) | GET |  |
| [List Domain Recipients](actions/list-domain-recipients.md) | GET |  |
| [List Recipients](actions/list-recipients.md) | GET |  |

### Sender Identity

| Action | Method | Description |
| --- | --- | --- |
| [Delete Sender Identity](actions/delete-sender-identity.md) | DELETE |  |
| [Get Sender Identity](actions/get-sender-identity.md) | GET |  |
| [List Sender Identities](actions/list-sender-identities.md) | GET |  |
| [Update Sender Identity](actions/update-sender-identity.md) | PUT |  |

### Template

| Action | Method | Description |
| --- | --- | --- |
| [Get Template](actions/get-template.md) | GET |  |
| [List Templates](actions/list-templates.md) | GET |  |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST |  |
| [Delete Webhook](actions/delete-webhook.md) | DELETE |  |
| [Get Webhook](actions/get-webhook.md) | GET |  |
| [List Webhooks](actions/list-webhooks.md) | GET |  |
| [Update Webhook](actions/update-webhook.md) | PUT |  |

