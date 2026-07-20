# Selzy: Native API Reference

A consolidated summary of Selzy's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://selzy.com/en/support/api/common/bulk-email/
- **API base URL:** `https://api.selzy.com/en/api`

## Authentication

### API Key

Use a Selzy API key from Settings -> Integration and API.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://selzy.com/en/support/api/common/api-key/)

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Cancel Campaign](actions/cancel-campaign.md) | `POST cancelCampaign` | [docs](https://selzy.com/en/support/api/messages/cancelcampaign/) |
| [Check Email](actions/check-email.md) | `POST checkEmail` | [docs](https://selzy.com/en/support/api/messages/checkemail/) |
| [Create Campaign](actions/create-campaign.md) | `POST createCampaign` | [docs](https://selzy.com/en/support/api/messages/createcampaign/) |
| [Create Contact Field](actions/create-contact-field.md) | `POST createField` | [docs](https://selzy.com/en/support/api/inputs/createfield/) |
| [Create Contact List](actions/create-contact-list.md) | `POST createList` | [docs](https://selzy.com/en/support/api/contacts/createlist/) |
| [Create Email Message](actions/create-email-message.md) | `POST createEmailMessage` | [docs](https://selzy.com/en/support/api/messages/createemailmessage/) |
| [Delete Contact List](actions/delete-contact-list.md) | `POST deleteList` | [docs](https://selzy.com/en/support/api/contacts/deletelist/) |
| [Delete Message](actions/delete-message.md) | `POST deleteMessage` | [docs](https://selzy.com/en/support/api/messages/deletemessage/) |
| [Exclude Contact](actions/exclude-contact.md) | `POST exclude` | [docs](https://selzy.com/en/support/api/contacts/exclude/) |
| [Export Contacts](actions/export-contacts.md) | `POST exportContacts` | [docs](https://selzy.com/en/support/api/contacts/exportcontacts/) |
| [Get Campaign Common Stats](actions/get-campaign-common-stats.md) | `POST getCampaignCommonStats` | [docs](https://selzy.com/en/support/api/statistics/get-campaign-common-stats/) |
| [Get Campaign Delivery Stats](actions/get-campaign-delivery-stats.md) | `POST getCampaignDeliveryStats` | [docs](https://selzy.com/en/support/api/statistics/getcampaigndeliverystats/) |
| [Get Campaign Status](actions/get-campaign-status.md) | `POST getCampaignStatus` | [docs](https://selzy.com/en/support/api/statistics/getcampaignstatus/) |
| [Get Contact](actions/get-contact.md) | `POST getContact` | [docs](https://selzy.com/en/support/api/contacts/getcontact/) |
| [Get Contact Count](actions/get-contact-count.md) | `POST getContactCount` | [docs](https://selzy.com/en/support/api/contacts/getcontactcount/) |
| [Get Message](actions/get-message.md) | `POST getMessage` | [docs](https://selzy.com/en/support/api/statistics/getmessage-method/) |
| [Get Total Contact Count](actions/get-total-contact-count.md) | `POST getTotalContactsCount` | [docs](https://selzy.com/en/support/api/contacts/gettotalcontactscount/) |
| [Import Contacts](actions/import-contacts.md) | `POST importContacts` | [docs](https://selzy.com/en/support/api/contacts/importcontacts/) |
| [List Campaigns](actions/list-campaigns.md) | `POST getCampaigns` | [docs](https://selzy.com/en/support/api/statistics/getcampaigns/) |
| [List Contact Fields](actions/list-contact-fields.md) | `POST getFields` | [docs](https://selzy.com/en/support/api/inputs/getfields/) |
| [List Contact Lists](actions/list-contact-lists.md) | `POST getLists` | [docs](https://selzy.com/en/support/api/contacts/getlists/) |
| [List Messages](actions/list-messages.md) | `POST getMessages` | [docs](https://selzy.com/en/support/api/statistics/getmessages/) |
| [List Tags](actions/list-tags.md) | `POST getTags` | [docs](https://selzy.com/en/support/api/inputs/gettags/) |
| [Send Email](actions/send-email.md) | `POST sendEmail` | [docs](https://selzy.com/en/support/api/messages/sendemail/) |
| [Send Test Email](actions/send-test-email.md) | `POST sendTestEmail` | [docs](https://selzy.com/en/support/api/messages/sendtestemail/) |
| [Subscribe Contact](actions/subscribe-contact.md) | `POST subscribe` | [docs](https://selzy.com/en/support/api/contacts/subscribe/) |
| [Unsubscribe Contact](actions/unsubscribe-contact.md) | `POST unsubscribe` | [docs](https://selzy.com/en/support/api/contacts/unsubscribe/) |
| [Update Contact Field](actions/update-contact-field.md) | `POST updateField` | [docs](https://selzy.com/en/support/api/inputs/updatefield/) |
| [Update Contact List](actions/update-contact-list.md) | `POST updateList` | [docs](https://selzy.com/en/support/api/contacts/updatelist/) |
| [Update Email Message](actions/update-email-message.md) | `POST updateEmailMessage` | [docs](https://selzy.com/en/support/api/messages/updateemailmessage/) |
