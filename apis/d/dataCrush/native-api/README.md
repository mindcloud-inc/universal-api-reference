# DataCrush: Native API Reference

A consolidated summary of DataCrush's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://help.datacrush.la/hc/es-419/categories/360004031271-Base-de-Conocimientos
- **API base URL:** `https://api.datacrush.la`

## Authentication

### Portal API Key

Authenticate with DataCrush using the support-issued portal_id and api_key required on every API request.

### Credentials

- **Portal ID:** `portalId` · required · Support-issued DataCrush portal identifier required on every API request.
- **API Key:** `apiKey` · required · Support-issued DataCrush API key required on every API request.

[Official authentication documentation](https://help.datacrush.la/hc/es-419/articles/360048047972--API-REST-v1-Contactos-Manejo-y-b%C3%BAsqueda-de-contactos-con-la-API-de-DataCrush)

## API conventions

Request bodies use URL-encoded form data.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Contact To Account](actions/add-contact-to-account.md) | `POST /account/contact-add` | [docs](https://help.datacrush.la/hc/es-419/articles/360048541991-API-REST-v1-Cuentas-Manejo-y-b%C3%BAsqueda-de-cuentas-con-la-API-de-DataCrush) |
| [Add Contact To Opportunity](actions/add-contact-to-opportunity.md) | `POST /crm/opportunity/contact-add` | [docs](https://help.datacrush.la/hc/es-419/articles/360048050372-API-REST-v1-Oportunidades-Manejo-y-b%C3%BAsqueda-de-oportunidades-con-la-API-de-DataCrush) |
| [Search Contacts By Lifecycle](actions/change-contact-email.md) | `POST /contact/search` | [docs](https://help.datacrush.la/hc/es-419/articles/360048047972--API-REST-v1-Contactos-Manejo-y-b%C3%BAsqueda-de-contactos-con-la-API-de-DataCrush) |
| [Change Opportunity Stage](actions/change-opportunity-stage.md) | `POST /crm/opportunity/stage` | [docs](https://help.datacrush.la/hc/es-419/articles/360048050372-API-REST-v1-Oportunidades-Manejo-y-b%C3%BAsqueda-de-oportunidades-con-la-API-de-DataCrush) |
| [Create Account](actions/create-account.md) | `POST /account/insert` | [docs](https://help.datacrush.la/hc/es-419/articles/360048541991-API-REST-v1-Cuentas-Manejo-y-b%C3%BAsqueda-de-cuentas-con-la-API-de-DataCrush) |
| [Create Contact](actions/create-contact.md) | `POST /contact/insert` | [docs](https://help.datacrush.la/hc/es-419/articles/360048047972--API-REST-v1-Contactos-Manejo-y-b%C3%BAsqueda-de-contactos-con-la-API-de-DataCrush) |
| [Create Ecommerce Category](actions/create-ecommerce-category.md) | `POST /ecommerce/v1/category/add` | [docs](https://help.datacrush.la/hc/es-419/articles/35071971467405-API-Ecommerce-Categor%C3%ADas) |
| [Create Ecommerce Customer](actions/create-ecommerce-customer.md) | `POST /ecommerce/v1/customer/add` | [docs](https://help.datacrush.la/hc/es-419/articles/35073317623693-API-Ecommerce-Clientes) |
| [Create Ecommerce Order](actions/create-ecommerce-order.md) | `POST /ecommerce/v1/order/add` | [docs](https://help.datacrush.la/hc/es-419/articles/35072600431501-API-Ecommerce-Pedidos) |
| [Create Ecommerce Product](actions/create-ecommerce-product.md) | `POST /ecommerce/v1/product/add` | [docs](https://help.datacrush.la/hc/es-419/articles/35072354545165-API-Ecommerce-Productos) |
| [Create Opportunity](actions/create-opportunity.md) | `POST /crm/opportunity/insert` | [docs](https://help.datacrush.la/hc/es-419/articles/360048050372-API-REST-v1-Oportunidades-Manejo-y-b%C3%BAsqueda-de-oportunidades-con-la-API-de-DataCrush) |
| [Delete Account](actions/delete-account.md) | `POST /account/delete` | [docs](https://help.datacrush.la/hc/es-419/articles/360048541991-API-REST-v1-Cuentas-Manejo-y-b%C3%BAsqueda-de-cuentas-con-la-API-de-DataCrush) |
| [Delete Contact](actions/delete-contact.md) | `POST /contact/delete` | [docs](https://help.datacrush.la/hc/es-419/articles/360048047972--API-REST-v1-Contactos-Manejo-y-b%C3%BAsqueda-de-contactos-con-la-API-de-DataCrush) |
| [Delete Opportunity](actions/delete-opportunity.md) | `POST /crm/opportunity/delete` | [docs](https://help.datacrush.la/hc/es-419/articles/360048050372-API-REST-v1-Oportunidades-Manejo-y-b%C3%BAsqueda-de-oportunidades-con-la-API-de-DataCrush) |
| [Search Contacts By Email](actions/import-contacts.md) | `POST /contact/search` | [docs](https://help.datacrush.la/hc/es-419/articles/360048047972--API-REST-v1-Contactos-Manejo-y-b%C3%BAsqueda-de-contactos-con-la-API-de-DataCrush) |
| [Search Accounts By Domain](actions/import-contacts-to-existing-list.md) | `POST /account/search` | [docs](https://help.datacrush.la/hc/es-419/articles/360048541991-API-REST-v1-Cuentas-Manejo-y-b%C3%BAsqueda-de-cuentas-con-la-API-de-DataCrush) |
| [Search Contacts By Contact Key](actions/ingest-contact-event.md) | `POST /contact/search` | [docs](https://help.datacrush.la/hc/es-419/articles/360048047972--API-REST-v1-Contactos-Manejo-y-b%C3%BAsqueda-de-contactos-con-la-API-de-DataCrush) |
| [Remove Contact From Account](actions/remove-contact-from-account.md) | `POST /account/contact-delete` | [docs](https://help.datacrush.la/hc/es-419/articles/360048541991-API-REST-v1-Cuentas-Manejo-y-b%C3%BAsqueda-de-cuentas-con-la-API-de-DataCrush) |
| [Remove Contact From Opportunity](actions/remove-contact-from-opportunity.md) | `POST /crm/opportunity/contact-delete` | [docs](https://help.datacrush.la/hc/es-419/articles/360048050372-API-REST-v1-Oportunidades-Manejo-y-b%C3%BAsqueda-de-oportunidades-con-la-API-de-DataCrush) |
| [Search Accounts](actions/search-accounts.md) | `POST /account/search` | [docs](https://help.datacrush.la/hc/es-419/articles/360048541991-API-REST-v1-Cuentas-Manejo-y-b%C3%BAsqueda-de-cuentas-con-la-API-de-DataCrush) |
| [Search Contacts](actions/search-contacts.md) | `POST /contact/search` | [docs](https://help.datacrush.la/hc/es-419/articles/360048047972--API-REST-v1-Contactos-Manejo-y-b%C3%BAsqueda-de-contactos-con-la-API-de-DataCrush) |
| [Search Contacts In List](actions/search-contacts-in-list.md) | `POST /contact/search` | [docs](https://help.datacrush.la/hc/es-419/articles/360048047972--API-REST-v1-Contactos-Manejo-y-b%C3%BAsqueda-de-contactos-con-la-API-de-DataCrush) |
| [Search Opportunities](actions/search-opportunities.md) | `POST /crm/opportunity/search` | [docs](https://help.datacrush.la/hc/es-419/articles/360048050372-API-REST-v1-Oportunidades-Manejo-y-b%C3%BAsqueda-de-oportunidades-con-la-API-de-DataCrush) |
| [Update Account](actions/update-account.md) | `POST /account/update` | [docs](https://help.datacrush.la/hc/es-419/articles/360048541991-API-REST-v1-Cuentas-Manejo-y-b%C3%BAsqueda-de-cuentas-con-la-API-de-DataCrush) |
| [Update Contact](actions/update-contact.md) | `POST /contact/update` | [docs](https://help.datacrush.la/hc/es-419/articles/360048047972--API-REST-v1-Contactos-Manejo-y-b%C3%BAsqueda-de-contactos-con-la-API-de-DataCrush) |
| [Update Ecommerce Category](actions/update-ecommerce-category.md) | `POST /ecommerce/v1/category/add` | [docs](https://help.datacrush.la/hc/es-419/articles/35071971467405-API-Ecommerce-Categor%C3%ADas) |
| [Update Ecommerce Customer](actions/update-ecommerce-customer.md) | `POST /ecommerce/v1/customer/add` | [docs](https://help.datacrush.la/hc/es-419/articles/35073317623693-API-Ecommerce-Clientes) |
| [Update Ecommerce Order](actions/update-ecommerce-order.md) | `POST /ecommerce/v1/order/add` | [docs](https://help.datacrush.la/hc/es-419/articles/35072600431501-API-Ecommerce-Pedidos) |
| [Update Ecommerce Product](actions/update-ecommerce-product.md) | `POST /ecommerce/v1/product/add` | [docs](https://help.datacrush.la/hc/es-419/articles/35072354545165-API-Ecommerce-Productos) |
| [Update Opportunity](actions/update-opportunity.md) | `POST /crm/opportunity/update` | [docs](https://help.datacrush.la/hc/es-419/articles/360048050372-API-REST-v1-Oportunidades-Manejo-y-b%C3%BAsqueda-de-oportunidades-con-la-API-de-DataCrush) |
