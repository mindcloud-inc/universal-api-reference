# Unisender: Native API Reference

A consolidated summary of Unisender's API configuration and 32 documented operations, with links to official documentation.

- **Official docs:** https://www.unisender.com/ru/support/api/
- **API base URL:** `https://api.unisender.com/en/api`

## Authentication

### API Key

Authenticate with a Unisender API key sent as the api_key query parameter on every request.

### Credentials

- **API Key:** `apiKey` · required · Paste the Unisender API key that Unisender's API key guide tells you to copy.

[Official authentication documentation](https://www.unisender.com/ru/support/api/common/api-key/)

## Endpoints (32 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Check Email](actions/check-email.md) | `GET /checkEmail` | [docs](https://www.unisender.com/ru/support/api/messages/check-email/) |
| [Check SMS](actions/check-sms.md) | `GET /checkSms` | [docs](https://www.unisender.com/ru/support/api/messages/check-sms/) |
| [Create List](actions/create-list.md) | `POST /createList` | [docs](https://www.unisender.com/ru/support/api/contacts/createlist/) |
| [Delete List](actions/delete-list.md) | `POST /deleteList` | [docs](https://www.unisender.com/ru/support/api/contacts/deletelist/) |
| [Export Contacts](actions/export-contacts.md) | `POST /exportContacts` | [docs](https://www.unisender.com/ru/support/api/contacts/exportcontacts/) |
| [Get Actual Message Version](actions/get-actual-message-version.md) | `GET /getActualMessageVersion` | [docs](https://www.unisender.com/ru/support/api/messages/get-actual-message-version/) |
| [Get Campaign Common Stats](actions/get-campaign-common-stats.md) | `GET /getCampaignCommonStats` | [docs](https://www.unisender.com/ru/support/api/statistics/get-campaign-common-stats/) |
| [Get Campaign Delivery Stats](actions/get-campaign-delivery-stats.md) | `GET /getCampaignDeliveryStats` | [docs](https://www.unisender.com/ru/support/api/statistics/getcampaigndeliverystats/) |
| [Get Campaign Status](actions/get-campaign-status.md) | `GET /getCampaignStatus` | [docs](https://www.unisender.com/ru/support/api/statistics/getcampaignstatus/) |
| [Get Campaigns](actions/get-campaigns.md) | `GET /getCampaigns` | [docs](https://www.unisender.com/ru/support/api/statistics/getcampaigns/) |
| [Get Contact](actions/get-contact.md) | `GET /getContact` | [docs](https://www.unisender.com/ru/support/api/contacts/getcontact/) |
| [Get Contact Count](actions/get-contact-count.md) | `GET /getContactCount` | [docs](https://www.unisender.com/ru/support/api/contacts/getcontactcount/) |
| [Get Contact Field Values](actions/get-contact-field-values.md) | `GET /getContactFieldValues` | [docs](https://www.unisender.com/ru/support/api/inputs/getcontactfieldvalues/) |
| [Get Fields](actions/get-fields.md) | `GET /getFields` | [docs](https://www.unisender.com/ru/support/api/inputs/getfields/) |
| [Get Message](actions/get-message.md) | `GET /getMessage` | [docs](https://www.unisender.com/ru/support/api/statistics/getmessage/) |
| [Get Messages](actions/get-messages.md) | `GET /getMessages` | [docs](https://www.unisender.com/ru/support/api/statistics/getmessages/) |
| [Get Sender Domain List](actions/get-sender-domain-list.md) | `GET /getSenderDomainList` | [docs](https://www.unisender.com/ru/support/api/messages/getsenderdomainlist/) |
| [Get Subscriber Note](actions/get-subscriber-note.md) | `GET /getSubscriberNote` | [docs](https://www.unisender.com/ru/support/api/notes/getsubscribernote/) |
| [Get Subscriber Notes](actions/get-subscriber-notes.md) | `GET /getSubscriberNotes` | [docs](https://www.unisender.com/ru/support/api/notes/getsubscribernotes/) |
| [Get Tags](actions/get-tags.md) | `GET /getTags` | [docs](https://www.unisender.com/ru/support/api/inputs/gettags/) |
| [Get Template](actions/get-template.md) | `GET /getTemplate` | [docs](https://www.unisender.com/ru/support/api/templates/gettemplate/) |
| [Get Templates](actions/get-templates.md) | `GET /getTemplates` | [docs](https://www.unisender.com/ru/support/api/templates/gettemplates/) |
| [Get Total Contacts Count](actions/get-total-contacts-count.md) | `GET /getTotalContactsCount` | [docs](https://www.unisender.com/ru/support/api/contacts/gettotalcontactscount/) |
| [Get Visited Links](actions/get-visited-links.md) | `GET /getVisitedLinks` | [docs](https://www.unisender.com/ru/support/api/statistics/getvisitedlinks/) |
| [Get Web Version](actions/get-web-version.md) | `GET /getWebVersion` | [docs](https://www.unisender.com/ru/support/api/messages/getwebversion/) |
| [Is Contact In Lists](actions/is-contact-in-lists.md) | `GET /isContactInLists` | [docs](https://www.unisender.com/ru/support/api/contacts/iscontactinlists/) |
| [List Lists](actions/list-lists.md) | `GET /getLists` | [docs](https://www.unisender.com/ru/support/api/contacts/getlists/) |
| [List Messages](actions/list-messages.md) | `GET /listMessages` | [docs](https://www.unisender.com/ru/support/api/statistics/listmessages/) |
| [List Templates](actions/list-templates.md) | `GET /listTemplates` | [docs](https://www.unisender.com/ru/support/api/templates/listtemplates/) |
| [Subscribe Contact](actions/subscribe-contact.md) | `POST /subscribe` | [docs](https://www.unisender.com/ru/support/api/contacts/subscribe/) |
| [Unsubscribe Contact](actions/unsubscribe-contact.md) | `POST /unsubscribe` | [docs](https://www.unisender.com/ru/support/api/contacts/unsubscribe/) |
| [Update List](actions/update-list.md) | `POST /updateList` | [docs](https://www.unisender.com/ru/support/api/contacts/updatelist/) |
