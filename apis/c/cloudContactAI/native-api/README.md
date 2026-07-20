# CloudContactAI: Native API Reference

A consolidated summary of CloudContactAI's API configuration and 37 documented operations, with links to official documentation.

- **Official docs:** https://developer.cloudcontactai.com/reference
- **API base URL:** `https://core.cloudcontactai.com`

## Authentication

### API Key

Use a CloudContactAI API key for bearer authentication. The tenant-specific client ID is required separately as a credential argument.

### Credentials

- **API Key:** `apiKey` · required
- **Client ID:** `clientId` · optional · The CloudContactAI tenant client ID. This value is sent in the required `clientId` header and used in client-scoped paths.

Send these headers with each API request:

```http
clientId: <clientId>
```

[Official authentication documentation](https://developer.cloudcontactai.com/reference)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (37 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Batch Create Contacts](actions/batch-create-contacts.md) | `POST api/v2/contacts/batch` | [docs](https://developer.cloudcontactai.com/reference) |
| [Create Campaign](actions/create-campaign.md) | `POST api/v2/campaigns` | [docs](https://developer.cloudcontactai.com/reference) |
| [Create Client](actions/create-client.md) | `POST api/clients` | [docs](https://developer.cloudcontactai.com/reference) |
| [Create Client Campaign](actions/create-client-campaign.md) | `POST api/clients/:clientId/campaigns` | [docs](https://developer.cloudcontactai.com/reference) |
| [Create Collection Campaign](actions/create-collection-campaign.md) | `POST api/v2/collection/campaign` | [docs](https://developer.cloudcontactai.com/reference) |
| [Create Contact](actions/create-contact.md) | `POST api/v2/contacts` | [docs](https://developer.cloudcontactai.com/reference) |
| [Create Direct Campaign](actions/create-direct-campaign.md) | `POST api/clients/:clientId/campaigns/direct` | [docs](https://developer.cloudcontactai.com/reference) |
| [Delete Campaign by ID](actions/delete-campaign-by-id.md) | `DELETE api/campaigns/:campaignId` | [docs](https://developer.cloudcontactai.com/reference) |
| [Delete Client by ID](actions/delete-client-by-id.md) | `DELETE api/clients/:id` | [docs](https://developer.cloudcontactai.com/reference) |
| [Delete Contact by ID](actions/delete-contact-by-id.md) | `DELETE api/v2/contacts/:id` | [docs](https://developer.cloudcontactai.com/reference) |
| [Get Campaign Contact Message](actions/get-campaign-contact-message.md) | `GET api/v2/messages/campaign/:campaignId/contact/:contactId` | [docs](https://developer.cloudcontactai.com/reference) |
| [Get Campaign Message Stats](actions/get-campaign-message-stats.md) | `GET api/v2/messages/campaign/:campaignId/stats` | [docs](https://developer.cloudcontactai.com/reference) |
| [Get Client by ID](actions/get-client-by-id.md) | `GET api/clients/:id` | [docs](https://developer.cloudcontactai.com/reference) |
| [Get Collection Client Settings](actions/get-collection-client-settings.md) | `GET api/v2/collection/client/settings` | [docs](https://developer.cloudcontactai.com/reference) |
| [Get Collection Debtor by Track ID](actions/get-collection-debtor-by-track-id.md) | `GET api/v2/collection/debtor/:trackId` | [docs](https://developer.cloudcontactai.com/reference) |
| [Get Contact by ID](actions/get-contact-by-id.md) | `GET api/v2/contacts/:id` | [docs](https://developer.cloudcontactai.com/reference) |
| [Get Contact Call Record](actions/get-contact-call-record.md) | `GET api/v2/contacts/:id/callRecord` | [docs](https://developer.cloudcontactai.com/reference) |
| [Get Message by ID](actions/get-message-by-id.md) | `GET api/v2/messages/:id` | [docs](https://developer.cloudcontactai.com/reference) |
| [List Campaigns](actions/list-campaigns.md) | `GET api/v2/campaigns` | [docs](https://developer.cloudcontactai.com/reference) |
| [List Client Campaigns](actions/list-client-campaigns.md) | `GET api/clients/:id/campaigns` | [docs](https://developer.cloudcontactai.com/reference) |
| [List Clients](actions/list-clients.md) | `GET api/clients` | [docs](https://developer.cloudcontactai.com/reference) |
| [List Contacts](actions/list-contacts.md) | `GET api/v2/contacts` | [docs](https://developer.cloudcontactai.com/reference) |
| [List Contacts with Email](actions/list-contacts-with-email.md) | `GET api/v2/contacts/withEmail` | [docs](https://developer.cloudcontactai.com/reference) |
| [List Contacts with Phone](actions/list-contacts-with-phone.md) | `GET api/v2/contacts/withPhone` | [docs](https://developer.cloudcontactai.com/reference) |
| [List Contacts without Call Record](actions/list-contacts-without-call-record.md) | `GET api/v2/contacts/withoutCallRecord` | [docs](https://developer.cloudcontactai.com/reference) |
| [List Incoming Messages](actions/list-incoming-messages.md) | `GET api/v2/messages/incoming` | [docs](https://developer.cloudcontactai.com/reference) |
| [List Messages by Campaign](actions/list-messages-by-campaign.md) | `GET api/v2/messages/campaign/:campaignId` | [docs](https://developer.cloudcontactai.com/reference) |
| [List Messages by Contact](actions/list-messages-by-contact.md) | `GET api/v2/messages/contact/:contactId` | [docs](https://developer.cloudcontactai.com/reference) |
| [List Sent Messages](actions/list-sent-messages.md) | `GET api/v2/messages/sent` | [docs](https://developer.cloudcontactai.com/reference) |
| [Patch Client by ID](actions/patch-client-by-id.md) | `PATCH api/clients/:id` | [docs](https://developer.cloudcontactai.com/reference) |
| [Requeue Campaign](actions/requeue-campaign.md) | `POST api/v2/campaigns/:campaignId/requeue` | [docs](https://developer.cloudcontactai.com/reference) |
| [Send Campaign Messages](actions/send-campaign-messages.md) | `POST api/v2/campaigns/messages` | [docs](https://developer.cloudcontactai.com/reference) |
| [Send Contact Message](actions/send-contact-message.md) | `POST api/v2/messages/contact/:contactId/send` | [docs](https://developer.cloudcontactai.com/reference) |
| [Update Client by ID](actions/update-client-by-id.md) | `PUT api/clients/:id` | [docs](https://developer.cloudcontactai.com/reference) |
| [Update Client Campaign](actions/update-client-campaign.md) | `PUT api/clients/:clientId/campaigns/:campaignId` | [docs](https://developer.cloudcontactai.com/reference) |
| [Update Collection Client Settings](actions/update-collection-client-settings.md) | `POST api/v2/collection/client/settings` | [docs](https://developer.cloudcontactai.com/reference) |
| [Update Contact by ID](actions/update-contact-by-id.md) | `PUT api/v1/contacts/:contact_id` | [docs](https://developer.cloudcontactai.com/reference) |
