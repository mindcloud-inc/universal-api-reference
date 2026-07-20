# Flexmail: Native API Reference

A consolidated summary of Flexmail's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://api.flexmail.eu/documentation/
- **OpenAPI specification:** https://api.flexmail.eu/documentation/openapi.json
- **API base URL:** `https://api.flexmail.eu`

## Authentication

### Basic

Use your Flexmail account ID as username and your personal access token as password.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://en.support.flexmail.eu/article/1242-getting-started-with-the-flexmail-transactional-api)

## Pagination

Use `limit` in the query string to set the page size (accepted range 1–500). Use `offset` in the query string as the record offset; numbering starts at 0.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Contact Import Records](actions/add-contact-import-records.md) | `POST /contacts/imports/{id}/records` | [docs](https://api.flexmail.eu/documentation/#post-/contacts/imports/-id-/records) |
| [Create Contact](actions/create-contact.md) | `POST /contacts` | [docs](https://api.flexmail.eu/documentation/#post-/contacts) |
| [Create Contact Import](actions/create-contact-import.md) | `POST /contacts/imports` | [docs](https://api.flexmail.eu/documentation/#post-/contacts/imports) |
| [Create Interest Subscription](actions/create-interest-subscription.md) | `POST /contacts/{id}/interest-subscriptions` | [docs](https://api.flexmail.eu/documentation/#post-/contacts/-id-/interest-subscriptions) |
| [Create Webhook](actions/create-webhook.md) | `POST /webhooks` | [docs](https://api.flexmail.eu/documentation/#post-/webhooks) |
| [Delete Interest Subscription](actions/delete-interest-subscription.md) | `DELETE /contacts/{id}/interest-subscriptions/{interest_id}` | [docs](https://api.flexmail.eu/documentation/#delete-/contacts/-id-/interest-subscriptions/-interest_id-) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE /webhooks/{id}` | [docs](https://api.flexmail.eu/documentation/#delete-/webhooks/-id-) |
| [Get Contact](actions/get-contact.md) | `GET /contacts/{id}` | [docs](https://api.flexmail.eu/documentation/#get-/contacts/-id-) |
| [Get Contact Import](actions/get-contact-import.md) | `GET /contacts/imports/{id}` | [docs](https://api.flexmail.eu/documentation/#get-/contacts/imports/-id-) |
| [Get Webhook](actions/get-webhook.md) | `GET /webhooks/{id}` | [docs](https://api.flexmail.eu/documentation/#get-/webhooks/-id-) |
| [List Contact Interest Subscriptions](actions/list-contact-interest-subscriptions.md) | `GET /contacts/{id}/interest-subscriptions` | [docs](https://api.flexmail.eu/documentation/#get-/contacts/-id-/interest-subscriptions) |
| [List Contacts](actions/list-contacts.md) | `GET /contacts` | [docs](https://api.flexmail.eu/documentation/#get-/contacts) |
| [List Custom Fields](actions/list-custom-fields.md) | `GET /custom-fields` | [docs](https://api.flexmail.eu/documentation/#get-/custom-fields) |
| [List Interests](actions/list-interests.md) | `GET /interests` | [docs](https://api.flexmail.eu/documentation/#get-/interests) |
| [List Opt-In Forms](actions/list-opt-in-forms.md) | `GET /opt-in-forms` | [docs](https://api.flexmail.eu/documentation/#get-/opt-in-forms) |
| [List Segments](actions/list-segments.md) | `GET /segments` | [docs](https://api.flexmail.eu/documentation/#get-/segments) |
| [List Sources](actions/list-sources.md) | `GET /sources` | [docs](https://api.flexmail.eu/documentation/#get-/sources) |
| [List Webhooks](actions/list-webhooks.md) | `GET /webhooks` | [docs](https://api.flexmail.eu/documentation/#get-/webhooks) |
| [Replace Contact](actions/replace-contact.md) | `PUT /contacts/{id}` | [docs](https://api.flexmail.eu/documentation/#put-/contacts/-id-) |
| [Start Contact Import](actions/start-contact-import.md) | `POST /contacts/imports/{id}/start` | [docs](https://api.flexmail.eu/documentation/#post-/contacts/imports/-id-/start) |
| [Submit Opt-In](actions/submit-opt-in.md) | `POST /opt-ins` | [docs](https://api.flexmail.eu/documentation/#post-/opt-ins) |
| [Unsubscribe Contact](actions/unsubscribe-contact.md) | `POST /contacts/{id}/unsubscribe` | [docs](https://api.flexmail.eu/documentation/#post-/contacts/-id-/unsubscribe) |
| [Update Contact](actions/update-contact.md) | `PATCH /contacts/{id}` | [docs](https://api.flexmail.eu/documentation/#patch-/contacts/-id-) |
| [Update Webhook](actions/update-webhook.md) | `PATCH /webhooks/{id}` | [docs](https://api.flexmail.eu/documentation/#patch-/webhooks/-id-) |
