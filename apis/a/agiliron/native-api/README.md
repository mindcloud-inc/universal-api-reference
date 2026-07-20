# Agiliron: Native API Reference

A consolidated summary of Agiliron's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://api.agiliron.com/reference
- **OpenAPI specification:** https://api.agiliron.com/docs/open-api-spec-37
- **API base URL:** `https://{yourCompany}.agiliron.net/agiliron/api-40.php/`

## Authentication

### API Key

Authenticate with Agiliron API key credentials.

### Credentials

- **API Key:** `apiKey` · required
- **Company Subdomain:** `yourCompany` · required · Your Agiliron company subdomain used in the API base URL.
- **API Key:** `key` · required · Agiliron API key generated from API Key Access Controls.

Send these headers with each API request:

```http
apiKey: <key>
```

[Official authentication documentation](https://learn.agiliron.com/docs/new-api-key-support-api40-manage-api-keys-and-access-permissions)

## API conventions

Responses from this API use XML.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Account](actions/add-account.md) | `POST Accounts` | [docs](https://api.agiliron.com/docs/add-account-1) |
| [Add Contact](actions/add-contact.md) | `POST Contact` | [docs](https://api.agiliron.com/docs/add-contact-1) |
| [Add Lead](actions/add-lead.md) | `POST Leads` | [docs](https://api.agiliron.com/docs/add-lead-1) |
| [Add Product](actions/add-product.md) | `POST Products` | [docs](https://api.agiliron.com/docs/add-product-2) |
| [Add Product Inventory](actions/add-product-inventory.md) | `POST ProductsInventory` | [docs](https://api.agiliron.com/docs/add-product-inventory-1) |
| [Add PurchaseOrder](actions/add-purchase-order.md) | `POST PurchaseOrder` | [docs](https://api.agiliron.com/docs/add-purchaseorder-1) |
| [Add Quote](actions/add-quote.md) | `POST Quote` | [docs](https://api.agiliron.com/docs/add-quote-1) |
| [Add SalesOrder](actions/add-sales-order.md) | `POST SalesOrder` | [docs](https://api.agiliron.com/docs/add-salesorder-1) |
| [Add Vendor](actions/add-vendor.md) | `POST Vendor` | [docs](https://api.agiliron.com/docs/add-vendor-1) |
| [Read Account](actions/read-account.md) | `GET Accounts` | [docs](https://api.agiliron.com/docs/read-account-1) |
| [Read Contact](actions/read-contact.md) | `GET Contact` | [docs](https://api.agiliron.com/docs/read-contact-1) |
| [Read Lead](actions/read-lead.md) | `GET Lead` | [docs](https://api.agiliron.com/docs/read-lead-1) |
| [Read Product](actions/read-product.md) | `GET Products` | [docs](https://api.agiliron.com/docs/read-product-1) |
| [Read Product Inventory](actions/read-product-inventory.md) | `GET ProductsInventory` | [docs](https://api.agiliron.com/docs/read-product-inventory) |
| [Read PurchaseOrder](actions/read-purchase-order.md) | `GET PurchaseOrder` | [docs](https://api.agiliron.com/docs/read-purchaseorder-1) |
| [Read Quote](actions/read-quote.md) | `GET Quote` | [docs](https://api.agiliron.com/docs/read-quote-1) |
| [Read SalesOrder](actions/read-sales-order.md) | `GET SalesOrder` | [docs](https://api.agiliron.com/docs/read-salesorder-1) |
| [Read Vendor](actions/read-vendor.md) | `GET Vendor` | [docs](https://api.agiliron.com/docs/read-vendor) |
| [Update Account](actions/update-account.md) | `PUT Accounts` | [docs](https://api.agiliron.com/docs/update-account-1) |
| [Update Contact](actions/update-contact.md) | `PUT Contact` | [docs](https://api.agiliron.com/docs/update-contact-1) |
| [Update Lead](actions/update-lead.md) | `PUT Leads` | [docs](https://api.agiliron.com/docs/update-lead-1) |
| [Update Product](actions/update-product.md) | `POST Products` | [docs](https://api.agiliron.com/docs/update-product-2) |
| [Update PurchaseOrder](actions/update-purchase-order.md) | `PUT PurchaseOrder` | [docs](https://api.agiliron.com/docs/update-purchaseorder-1) |
| [Update SalesOrder](actions/update-sales-order.md) | `PUT SalesOrder` | [docs](https://api.agiliron.com/docs/update-salesorder-1) |
