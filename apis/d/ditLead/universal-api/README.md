# <img src="https://images.mindcloud.co/apps/icons/dit-lead_1775067786842.png" alt="DitLead logo" width="28" height="28"> DitLead: Universal API

DitLead is a multi-channel outreach platform with contacts, lists, campaigns, mailbox health checks, email verification, and webhook automation APIs.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/ditLead/latest
- **Category:** Marketing
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://ditlead.com
- **Vendor API docs:** https://ditlead.com/developer/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Validate API Key](actions/validate-api-key.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ditLead/latest/actions/validate-api-key?connectionId=$CONNECTION_ID&keyType=platform" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### API Keys

| Action | Method | Description |
| --- | --- | --- |
| [Validate API Key](actions/validate-api-key.md) | GET |  |

### Campaigns

| Action | Method | Description |
| --- | --- | --- |
| [Get Campaigns](actions/get-campaigns.md) | GET |  |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Add Contact To List](actions/add-contact-to-list.md) | PUT |  |
| [Create Contact](actions/create-contact.md) | POST |  |
| [Delete Contact](actions/delete-contact.md) | DELETE |  |
| [Get Contact](actions/get-contact.md) | GET |  |
| [Get Contacts](actions/get-contacts.md) | GET |  |
| [Remove Contact From List](actions/remove-contact-from-list.md) | PUT |  |
| [Update Contact](actions/update-contact.md) | PUT |  |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Check Mailbox DKIM](actions/check-mailbox-dkim.md) | GET |  |
| [Check Mailbox DMARC](actions/check-mailbox-dmarc.md) | GET |  |
| [Check Mailbox SPF](actions/check-mailbox-spf.md) | GET |  |
| [Create List](actions/create-list.md) | POST |  |
| [Create Mailbox](actions/create-mailbox.md) | POST |  |
| [Delete List](actions/delete-list.md) | DELETE |  |
| [Delete Mailbox](actions/delete-mailbox.md) | DELETE |  |
| [Get List](actions/get-list.md) | GET |  |
| [Get Lists](actions/get-lists.md) | GET |  |
| [Get Mailbox](actions/get-mailbox.md) | GET |  |
| [Get Mailbox Insight](actions/get-mailbox-insight.md) | GET |  |
| [Get Mailboxes](actions/get-mailboxes.md) | GET |  |
| [Reconnect Mailbox](actions/reconnect-mailbox.md) | PUT |  |
| [Send Warming Emails](actions/send-warming-emails.md) | PUT |  |
| [Set Mailbox Warming](actions/set-mailbox-warming.md) | PUT |  |
| [Update Mailbox](actions/update-mailbox.md) | PUT |  |
| [Validate Mailbox SMTP IMAP](actions/validate-mailbox-smtp-imap.md) | GET |  |
| [Verify Email](actions/verify-email.md) | GET |  |

### Webhook Endpoints

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook Subscription](actions/create-webhook-subscription.md) | POST |  |
| [Delete Webhook Subscription](actions/delete-webhook-subscription.md) | DELETE |  |
| [Get Webhook Subscription](actions/get-webhook-subscription.md) | GET |  |

