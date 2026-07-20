# BlueFox Email: Native API Reference

A consolidated summary of BlueFox Email's API configuration and 14 documented operations, with links to official documentation.

- **Official docs:** https://bluefox.email/docs/api/
- **API base URL:** `https://api.bluefox.email`

## Authentication

### API Key

Connect with a BlueFox project API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://bluefox.email/docs/projects/settings)

## Endpoints (14 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Activate Subscription](actions/activate-subscription.md) | `PATCH /v1/subscriber-lists/:subscriberListId/:subscriberEmailAddress` | [docs](https://bluefox.email/docs/api/subscriber-list-management#activate-subscription) |
| [Create Contact](actions/create-contact.md) | `POST /v1/contacts/:projectId` | [docs](https://bluefox.email/docs/api/contacts-management#create-contact) |
| [Delete Contact](actions/delete-contact.md) | `DELETE /v1/contacts/:projectId/:contactEmailAddress` | [docs](https://bluefox.email/docs/api/contacts-management#delete-contact) |
| [Get Contact](actions/get-contact.md) | `GET /v1/contacts/:projectId/:contactEmailAddress` | [docs](https://bluefox.email/docs/api/contacts-management#get-one-contact) |
| [Get Subscriber](actions/get-subscriber.md) | `GET /v1/subscriber-lists/:subscriberListId/:subscriberEmailAddress` | [docs](https://bluefox.email/docs/api/subscriber-list-management#get-one-subscriber) |
| [List Contacts](actions/list-contacts.md) | `GET /v1/contacts/:projectId` | [docs](https://bluefox.email/docs/api/contacts-management#list-contacts) |
| [List Subscribers](actions/list-subscribers.md) | `GET /v1/subscriber-lists/:subscriberListId` | [docs](https://bluefox.email/docs/api/subscriber-list-management#list-subscribers) |
| [Pause Subscription](actions/pause-subscription.md) | `PATCH /v1/subscriber-lists/:subscriberListId/:subscriberEmailAddress` | [docs](https://bluefox.email/docs/api/subscriber-list-management#pause-subscription) |
| [Send Transactional Email](actions/send-transactional-email.md) | `POST /v1/send-transactional` | [docs](https://bluefox.email/docs/api/send-transactional-email) |
| [Send Triggered Email](actions/send-triggered-email.md) | `POST /v1/send-triggered` | [docs](https://bluefox.email/docs/api/send-triggered-email) |
| [Subscribe](actions/subscribe.md) | `POST /v1/subscriber-lists/:subscriberListId` | [docs](https://bluefox.email/docs/api/subscriber-list-management#subscribe) |
| [Unsubscribe](actions/unsubscribe.md) | `PATCH /v1/subscriber-lists/:subscriberListId/:subscriberEmailAddress` | [docs](https://bluefox.email/docs/api/subscriber-list-management#unsubscribe) |
| [Update Contact](actions/update-contact.md) | `PATCH /v1/contacts/:projectId/:contactEmailAddress` | [docs](https://bluefox.email/docs/api/contacts-management#update-contact) |
| [Update Subscriber](actions/update-subscriber.md) | `PATCH /v1/subscriber-lists/:subscriberListId/:subscriberEmailAddress` | [docs](https://bluefox.email/docs/api/subscriber-list-management#update-subscriber) |
