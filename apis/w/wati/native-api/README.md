# Wati: Native API Reference

A consolidated summary of Wati's API configuration and 14 documented operations, with links to official documentation.

- **Official docs:** https://docs.wati.io/reference
- **API base URL:** `{apiEndpointUrl}`

## Authentication

### API Access Token

Use a Wati API access token.

### Credentials

- **API Key:** `apiKey` · required
- **API Endpoint URL:** `apiEndpointUrl` · required · Tenant-specific Wati API endpoint URL, for example https://app-server.wati.io

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.wati.io/reference/authentication)

## API conventions

The current page number is read from `link.pageNumber`.

## Endpoints (14 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Contact](actions/add-contact.md) | `POST /api/v1/addContact/:whatsappNumber` | [docs](https://docs.wati.io/reference/post_api-v1-addcontact-whatsappnumber) |
| [Assign User](actions/assign-user.md) | `POST /api/v1/assignOperator` | [docs](https://docs.wati.io/reference/post_api-v1-assignoperator) |
| [Get Media by File Name](actions/get-media-by-file-name.md) | `GET /api/v1/getMedia` | [docs](https://docs.wati.io/reference/get_api-v1-getmedia) |
| [List Contacts](actions/list-contacts.md) | `GET /api/v1/getContacts` | [docs](https://docs.wati.io/reference/get_api-v1-getcontacts) |
| [List Message Templates](actions/list-message-templates.md) | `GET /api/v1/getMessageTemplates` | [docs](https://docs.wati.io/reference/get_api-v1-getmessagetemplates) |
| [List Messages by WhatsApp Number](actions/list-messages-by-whatsapp-number.md) | `GET /api/v1/getMessages/:whatsappNumber` | [docs](https://docs.wati.io/reference/get_api-v1-getmessages-whatsappnumber) |
| [Send File to Open Session](actions/send-file-to-open-session.md) | `POST /api/v1/sendSessionFile/:whatsappNumber` | [docs](https://docs.wati.io/reference/post_api-v1-sendsessionfile-whatsappnumber) |
| [Send Interactive Buttons Message](actions/send-interactive-buttons-message.md) | `POST /api/v1/sendInteractiveButtonsMessage` | [docs](https://docs.wati.io/reference/post_api-v1-sendinteractivebuttonsmessage) |
| [Send Interactive List Message](actions/send-interactive-list-message.md) | `POST /api/v1/sendInteractiveListMessage` | [docs](https://docs.wati.io/reference/post_api-v1-sendinteractivelistmessage) |
| [Send Message to Open Session](actions/send-message-to-open-session.md) | `POST /api/v1/sendSessionMessage/:whatsappNumber` | [docs](https://docs.wati.io/reference/post_api-v1-sendsessionmessage-whatsappnumber) |
| [Send Template Message](actions/send-template-message.md) | `POST /api/v1/sendTemplateMessage` | [docs](https://docs.wati.io/reference/post_api-v1-sendtemplatemessage) |
| [Send Template Messages](actions/send-template-messages.md) | `POST /api/v1/sendTemplateMessages` | [docs](https://docs.wati.io/reference/post_api-v1-sendtemplatemessages) |
| [Send Template Messages CSV](actions/send-template-messages-csv.md) | `POST /api/v1/sendTemplateMessageCSV` | [docs](https://docs.wati.io/reference/post_api-v1-sendtemplatemessagecsv) |
| [Update Contact Attributes](actions/update-contact-attributes.md) | `POST /api/v1/updateContactAttributes/:whatsappNumber` | [docs](https://docs.wati.io/reference/post_api-v1-updatecontactattributes-whatsappnumber) |
