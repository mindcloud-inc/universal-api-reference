# RAYNET CRM: Native API Reference

A consolidated summary of RAYNET CRM's API configuration and 26 documented operations, with links to official documentation.

- **Official docs:** https://app.raynetcrm.com/api/doc/index-en.html
- **API base URL:** `https://app.raynetcrm.com/api/v2/`

## Authentication

### Basic API Key

Connect Raynet CRM with an administrator username or email, a generated API key, and the tenant instance name used in the X-Instance-Name header.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required
- **Instance Name:** `instanceName` · required · Tenant instance name sent in the X-Instance-Name header on every request.

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://support.raynetcrm.com/hc/en-us/articles/360032478072-How-to-generate-an-API-key)

## Pagination

Use `limit` in the query string to set the page size (default 100; accepted range 1–1000). Use `offset` in the query string as the record offset; numbering starts at 0.

## Filtering

Send filters in the query string.

## Sorting

Set the sort field with `sortColumn` in the query string. Set the direction separately with `sortDirection`. Use `ASC` for ascending order and `DESC` for descending order. Only one sort field is accepted.

## Endpoints (26 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Convert Lead](actions/convert-lead.md) | `POST lead/:leadId/convert/` | [docs](https://app.raynetcrm.com/api/doc/index-en.html#tag/Leads/operation/leadConvert) |
| [Create Company](actions/create-company.md) | `PUT company/` | [docs](https://app.raynetcrm.com/api/doc/index-en.html#tag/Accounts/operation/companyInsert) |
| [Create Contact](actions/create-contact.md) | `PUT person/` | [docs](https://app.raynetcrm.com/api/doc/index-en.html#tag/Contacts/operation/personInsert) |
| [Create Deal](actions/create-deal.md) | `PUT businessCase/` | [docs](https://app.raynetcrm.com/api/doc/index-en.html#tag/Deals/operation/businessCaseInsert) |
| [Create Lead](actions/create-lead.md) | `PUT lead/` | [docs](https://app.raynetcrm.com/api/doc/index-en.html#tag/Leads/operation/leadInsert) |
| [Create Product](actions/create-product.md) | `PUT product/` | [docs](https://app.raynetcrm.com/api/doc/index-en.html#tag/Products/operation/productInsert) |
| [Create Webhook](actions/create-webhook.md) | `PUT webhook/` | [docs](https://app.raynetcrm.com/api/doc/index-en.html#tag/Webhook/operation/webhookInsert) |
| [Delete Company](actions/delete-company.md) | `DELETE company/:companyId/` | [docs](https://app.raynetcrm.com/api/doc/index-en.html#tag/Accounts/operation/companyDelete) |
| [Delete Contact](actions/delete-contact.md) | `DELETE person/:personId/` | [docs](https://app.raynetcrm.com/api/doc/index-en.html#tag/Contacts/operation/personDelete) |
| [Delete Deal](actions/delete-deal.md) | `DELETE businessCase/:businessCaseId/` | [docs](https://app.raynetcrm.com/api/doc/index-en.html#tag/Deals/operation/businessCaseDelete) |
| [Delete Lead](actions/delete-lead.md) | `DELETE lead/:leadId/` | [docs](https://app.raynetcrm.com/api/doc/index-en.html#tag/Leads/operation/leadDelete) |
| [Get Company](actions/get-company.md) | `GET company/:companyId/` | [docs](https://app.raynetcrm.com/api/doc/index-en.html#tag/Accounts/operation/companyDetailGet) |
| [Get Contact](actions/get-contact.md) | `GET person/:personId/` | [docs](https://app.raynetcrm.com/api/doc/index-en.html#tag/Contacts/operation/personDetailGet) |
| [Get Deal](actions/get-deal.md) | `GET businessCase/:businessCaseId/` | [docs](https://app.raynetcrm.com/api/doc/index-en.html#tag/Deals/operation/businessCaseDetailGet) |
| [Get Lead](actions/get-lead.md) | `GET lead/:leadId/` | [docs](https://app.raynetcrm.com/api/doc/index-en.html#tag/Leads/operation/leadDetailGet) |
| [Get Product](actions/get-product.md) | `GET product/:productId/` | [docs](https://app.raynetcrm.com/api/doc/index-en.html#tag/Products/operation/productDetailGet) |
| [List Companies](actions/list-companies.md) | `GET company/` | [docs](https://app.raynetcrm.com/api/doc/index-en.html#tag/Accounts/operation/companyGet) |
| [List Contacts](actions/list-contacts.md) | `GET person/` | [docs](https://app.raynetcrm.com/api/doc/index-en.html#tag/Contacts/operation/personGet) |
| [List Deals](actions/list-deals.md) | `GET businessCase/` | [docs](https://app.raynetcrm.com/api/doc/index-en.html#tag/Deals/operation/businessCaseGet) |
| [List Leads](actions/list-leads.md) | `GET lead/` | [docs](https://app.raynetcrm.com/api/doc/index-en.html#tag/Leads/operation/leadGet) |
| [List Products](actions/list-products.md) | `GET product/` | [docs](https://app.raynetcrm.com/api/doc/index-en.html#tag/Products/operation/productGet) |
| [List Webhooks](actions/list-webhooks.md) | `GET webhook/` | [docs](https://app.raynetcrm.com/api/doc/index-en.html#tag/Webhook/operation/webhookGet) |
| [Update Company](actions/update-company.md) | `POST company/:companyId/` | [docs](https://app.raynetcrm.com/api/doc/index-en.html#tag/Accounts/operation/companyEdit) |
| [Update Contact](actions/update-contact.md) | `POST person/:personId/` | [docs](https://app.raynetcrm.com/api/doc/index-en.html#tag/Contacts/operation/personEdit) |
| [Update Deal](actions/update-deal.md) | `POST businessCase/:businessCaseId/` | [docs](https://app.raynetcrm.com/api/doc/index-en.html#tag/Deals/operation/businessCaseEdit) |
| [Update Lead](actions/update-lead.md) | `POST lead/:leadId/` | [docs](https://app.raynetcrm.com/api/doc/index-en.html#tag/Leads/operation/leadEdit) |
