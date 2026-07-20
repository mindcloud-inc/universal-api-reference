# Alegra: Native API Reference

A consolidated summary of Alegra's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://developer.alegra.com/
- **API base URL:** `https://api.alegra.com/api/v1`

## Authentication

### Basic

HTTP Basic authentication using your Alegra account email as the username and your Alegra API token as the password.

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

[Official authentication documentation](https://developer.alegra.com/reference/autenticaci%C3%B3n)

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Bill](actions/create-bill.md) | `POST /bills` | [docs](https://developer.alegra.com/reference/post_bills) |
| [Create Contact](actions/create-contact.md) | `POST /contacts` | [docs](https://developer.alegra.com/reference/post_contacts) |
| [Create Invoice](actions/create-invoice.md) | `POST /invoices` | [docs](https://developer.alegra.com/reference/post_invoices) |
| [Create Item](actions/create-item.md) | `POST /items` | [docs](https://developer.alegra.com/reference/post_items) |
| [Create Payment](actions/create-payment.md) | `POST /payments` | [docs](https://developer.alegra.com/reference/post_payments) |
| [Create Webhook Subscription](actions/create-webhook-subscription.md) | `POST /webhooks/subscriptions` | [docs](https://developer.alegra.com/reference/post_webhooks-subscriptions) |
| [Delete Contact](actions/delete-contact.md) | `DELETE /contacts/:id` | [docs](https://developer.alegra.com/reference/deletecontact) |
| [Delete Invoice](actions/delete-invoice.md) | `DELETE /invoices/:id` | [docs](https://developer.alegra.com/reference/delete_invoices-id) |
| [Delete Item](actions/delete-item.md) | `DELETE /items/:id` | [docs](https://developer.alegra.com/reference/delete_items-id) |
| [Delete Payment](actions/delete-payment.md) | `DELETE /payments/:id` | [docs](https://developer.alegra.com/reference/delete_payments-id) |
| [Delete Webhook Subscription](actions/delete-webhook-subscription.md) | `DELETE /webhooks/subscriptions/:id` | [docs](https://developer.alegra.com/reference/delete_webhooks-subscriptions-id) |
| [Get Bill](actions/get-bill.md) | `GET /bills/:id` | [docs](https://developer.alegra.com/reference/get_bills-id) |
| [Get Company](actions/get-company.md) | `GET /company` | [docs](https://developer.alegra.com/reference/get_company-1) |
| [Get Contact](actions/get-contact.md) | `GET /contacts/:id` | [docs](https://developer.alegra.com/reference/contactsdetails-1) |
| [Get Invoice](actions/get-invoice.md) | `GET /invoices/:id` | [docs](https://developer.alegra.com/reference/get_invoices-id) |
| [Get Item](actions/get-item.md) | `GET /items/:id` | [docs](https://developer.alegra.com/reference/get_items-id) |
| [Get Payment](actions/get-payment.md) | `GET /payments/:id` | [docs](https://developer.alegra.com/reference/get_payments-id) |
| [List Bills](actions/list-bills.md) | `GET /bills` | [docs](https://developer.alegra.com/reference/get_bills) |
| [List Contacts](actions/list-contacts.md) | `GET /contacts` | [docs](https://developer.alegra.com/reference/listcontacts-1) |
| [List Invoices](actions/list-invoices.md) | `GET /invoices` | [docs](https://developer.alegra.com/reference/get_invoices) |
| [List Items](actions/list-items.md) | `GET /items` | [docs](https://developer.alegra.com/reference/get_items) |
| [List Payments](actions/list-payments.md) | `GET /payments` | [docs](https://developer.alegra.com/reference/get_payments) |
| [List Webhook Subscriptions](actions/list-webhook-subscriptions.md) | `GET /webhooks/subscriptions` | [docs](https://developer.alegra.com/reference/get_webhooks-subscriptions) |
| [Restore Contact](actions/restore-contact.md) | `PUT /contacts/restore/:id` | [docs](https://developer.alegra.com/reference/restorecontact) |
| [Send Invoice Email](actions/send-invoice-email.md) | `POST /invoices/:id/email` | [docs](https://developer.alegra.com/reference/post_invoices-id-email) |
| [Update Bill](actions/update-bill.md) | `PUT /bills/:id` | [docs](https://developer.alegra.com/reference/put_bills-id) |
| [Update Contact](actions/update-contact.md) | `PUT /contacts/:id` | [docs](https://developer.alegra.com/reference/editcontact) |
| [Update Invoice](actions/update-invoice.md) | `PUT /invoices/:id` | [docs](https://developer.alegra.com/reference/put_invoices-id) |
| [Update Item](actions/update-item.md) | `PUT /items/:id` | [docs](https://developer.alegra.com/reference/put_items-id) |
| [Update Payment](actions/update-payment.md) | `PUT /payments/:id` | [docs](https://developer.alegra.com/reference/put_payments-id) |
