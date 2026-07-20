# Growby: Native API Reference

A consolidated summary of Growby's API configuration and 25 documented operations, with links to official documentation.

- **Official docs:** https://www.postman.com/growby-documentation/growby-api/documentation/i4ul9w0/growby-api
- **API base URL:** `https://api.growby.net`

## Authentication

### API Key

Use the Growby API key shown in the API Setup page.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
ApiKey: <apiKey>
```

[Official authentication documentation](https://www.postman.com/growby-documentation/growby-api/documentation/i4ul9w0/growby-api)

## API conventions

Responses from this API use JSON.

## Pagination

Use `pageSize` in the query string to set the page size (accepted range 1–20). Use `pageNumber` in the query string to choose the page; numbering starts at 1.

## Endpoints (25 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Contact To Group By Group ID](actions/add-contact-to-group-by-group-id.md) | `POST /groups/:groupId/contacts/:contactId` | [docs](https://www.postman.com/growby-documentation/growby-api/documentation/i4ul9w0/growby-api) |
| [Add Contact To Group By Group Name](actions/add-contact-to-group-by-group-name.md) | `POST /groups/:groupname/contacts/:contactId` | [docs](https://www.postman.com/growby-documentation/growby-api/documentation/i4ul9w0/growby-api) |
| [Bulk Add Contacts To Group By Group ID](actions/bulk-add-contacts-to-group-by-group-id.md) | `POST /groups/:groupId/contacts/:contactlist` | [docs](https://www.postman.com/growby-documentation/growby-api/documentation/i4ul9w0/growby-api) |
| [Bulk Add Contacts To Group By Group Name](actions/bulk-add-contacts-to-group-by-group-name.md) | `POST /groups/:groupname/contacts/:contactlist` | [docs](https://www.postman.com/growby-documentation/growby-api/documentation/i4ul9w0/growby-api) |
| [Create Contact](actions/create-contact.md) | `POST /devapi/AddContact` | [docs](https://www.postman.com/growby-documentation/growby-api/documentation/i4ul9w0/growby-api) |
| [Create Group](actions/create-group.md) | `POST /groups` | [docs](https://www.postman.com/growby-documentation/growby-api/documentation/i4ul9w0/growby-api) |
| [Delete Contact](actions/delete-contact.md) | `DELETE /devapi/contact/:id` | [docs](https://www.postman.com/growby-documentation/growby-api/documentation/i4ul9w0/growby-api) |
| [List Contacts](actions/list-contacts.md) | `GET /devapi/contacts` | [docs](https://www.postman.com/growby-documentation/growby-api/documentation/i4ul9w0/growby-api) |
| [List Groups](actions/list-groups.md) | `GET /groups` | [docs](https://www.postman.com/growby-documentation/growby-api/documentation/i4ul9w0/growby-api) |
| [List Message Templates](actions/list-message-templates.md) | `GET /v1/messages_templates` | [docs](https://www.postman.com/growby/workspace/growby/folder/29609016-ef13f103-ac66-4520-8ca0-5ec329e30d00) |
| [Send Carousel Template Message](actions/send-carousel-template-message.md) | `POST /v3/messages` | [docs](https://www.postman.com/growby-documentation/growby-api/request/0wp1j1j/send-carousel-template-message) |
| [Send Document Message](actions/send-document-message.md) | `POST /v3/messages` | [docs](https://www.postman.com/growby-documentation/growby-api/folder/l29qmmq/v3-messages) |
| [Send Image Reply Message](actions/send-image-reply-message.md) | `POST /v1/reply-messages` | [docs](https://www.postman.com/growby/workspace/growby/folder/29609016-3a876c37-d822-48be-b589-871f5fc2d7d6) |
| [Send Interactive Template Message](actions/send-interactive-template-message.md) | `POST /v3/messages` | [docs](https://www.postman.com/growby-documentation/growby-api/request/i5bqua7/send-interactive-template-message) |
| [Send Media Message](actions/send-media-message.md) | `POST /v3/messages` | [docs](https://www.postman.com/growby-documentation/growby-api/request/mugkxwl/send-media-message) |
| [Send Media Template Message](actions/send-media-template-message.md) | `POST /v3/messages` | [docs](https://www.postman.com/growby-documentation/growby-api/request/t228iu6/send-media-template-message) |
| [Send Media Template Message With Parameters](actions/send-media-template-message-with-parameters.md) | `POST /v1/messages` | [docs](https://www.postman.com/growby/workspace/growby/folder/29609016-3d951c54-49db-4942-ae2c-f1e767b3736c) |
| [Send Message V2](actions/send-message-v2.md) | `POST /v2/messages` | [docs](https://www.postman.com/growby-documentation/growby-api/folder/u5nohd1/send-message) |
| [Send Template Message](actions/send-template-message.md) | `POST /v1/messages` | [docs](https://www.postman.com/growby/workspace/growby/folder/29609016-3d951c54-49db-4942-ae2c-f1e767b3736c) |
| [Send Template Message With Parameters](actions/send-template-message-with-parameters.md) | `POST /v1/messages` | [docs](https://www.postman.com/growby/workspace/growby/folder/29609016-3d951c54-49db-4942-ae2c-f1e767b3736c) |
| [Send Text Message](actions/send-text-message.md) | `POST /v3/messages` | [docs](https://www.postman.com/growby-documentation/growby-api/request/84rvkmu/send-text-message) |
| [Send Text Reply Message](actions/send-text-reply-message.md) | `POST /v1/reply-messages` | [docs](https://www.postman.com/growby/workspace/growby/folder/29609016-3a876c37-d822-48be-b589-871f5fc2d7d6) |
| [Send Text Template Message](actions/send-text-template-message.md) | `POST /v3/messages` | [docs](https://www.postman.com/growby-documentation/growby-api/request/u5iw6ai/send-text-template-message) |
| [Send Video Message](actions/send-video-message.md) | `POST /v3/messages` | [docs](https://www.postman.com/growby-documentation/growby-api/folder/l29qmmq/v3-messages) |
| [Update Contact](actions/update-contact.md) | `PUT /devapi/contact/:id` | [docs](https://www.postman.com/growby-documentation/growby-api/documentation/i4ul9w0/growby-api) |
