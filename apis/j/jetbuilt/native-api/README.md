# Jetbuilt: Native API Reference

A consolidated summary of Jetbuilt's API configuration and 42 documented operations, with links to official documentation.

- **Official docs:** https://api.jetbuilt.com/customers#introduction
- **API base URL:** `https://app.jetbuilt.com/api/`

## Authentication

### API key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/vnd.jetbuilt.v1` |
| `Content-Type` | `application/json; charset=utf-8` |

## Pagination

Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (42 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create a Product](actions/create-a-product.md) | `POST product_databases/:productDatabaseId/products` |  |
| [Create a Project Revision](actions/create-a-project-revision.md) | `POST projects/:projectId/revisions` |  |
| [Create Client](actions/create-client.md) | `POST clients` |  |
| [Create Client Contact](actions/create-client-contact.md) | `POST clients/:client_id/contacts` |  |
| [Create Project](actions/create-project.md) | `POST projects` |  |
| [Create Project Item](actions/create-project-item.md) | `POST projects/:projectId/items` |  |
| [Create Project System](actions/create-project-system.md) | `GET` |  |
| [Get a Product](actions/get-a-product.md) | `GET product_databases/:databaseId/products/:id` |  |
| [Get a product for a vendor](actions/get-a-product-for-a-vendor.md) | `GET product_databases/:databaseId/vendors/:vendorId/products/:productId` | [docs](https://api.jetbuilt.com/customers#get-a-product-for-a-vendor) |
| [Get a Room](actions/get-a-room.md) | `GET projects/:projectId/rooms/:roomId` | [docs](https://api.jetbuilt.com/customers?shell--json#get-a-room-in-your-project) |
| [Get a Vendor](actions/get-a-vendor.md) | `GET product_databases/:databaseID/vendors/:vendorId` | [docs](https://api.jetbuilt.com/customers#get-a-vendor) |
| [Get All Products](actions/get-all-products.md) | `GET product_databases/:databaseId/products` | [docs](https://api.jetbuilt.com/customers#get-all-products) |
| [Get All Products for a Vendor](actions/get-all-products-for-a-vendor.md) | `GET product_databases/:dbid/vendors/:vendor/products` | [docs](https://api.jetbuilt.com/customers?shell--json#get-all-products-for-a-vendor) |
| [Get All Rooms](actions/get-all-rooms.md) | `GET projects/:project_id/rooms/` |  |
| [Get All Stock Items](actions/get-all-stock-items.md) | `GET stock/items` | [docs](https://api.jetbuilt.com/customers?shell--json#get-all-stock-items) |
| [Get All Stock Products](actions/get-all-stock-products.md) | `GET stock/products` | [docs](https://api.jetbuilt.com/customers?shell--json#get-all-stock-products) |
| [List Vendors](actions/get-all-vendors.md) | `GET product_databases/:dbId/vendors` | [docs](https://api.jetbuilt.com/customers#get-all-vendors) |
| [Get Client](actions/get-client.md) | `GET clients/:id` |  |
| [Get Client Contacts](actions/get-client-contacts.md) | `GET clients/[:id]/contacts` |  |
| [Get All Clients](actions/get-clients.md) | `GET clients` |  |
| [Get Company](actions/get-company.md) | `GET company` |  |
| [Get Labor Presets](actions/get-labor-presets.md) | `GET labor_presets/:laborPresetID` | [docs](https://api.jetbuilt.com/customers?shell--json#labor-presets) |
| [Get Market Segment](actions/get-market-segment.md) | `GET market_segments` |  |
| [Get Project Factors](actions/get-project-factors.md) | `GET projects/[:projectId]/items` |  |
| [Get Project Items](actions/get-project-items.md) | `GET projects/:projectId/items` | [docs](https://api.jetbuilt.com/customers?shell--json#project-items) |
| [Get Project Options](actions/get-project-options.md) | `GET projects/:projectId/options/[:optionId]` |  |
| [Get Project Purchasing](actions/get-project-purchasing.md) | `GET projects/[:projectId]/purchasing` |  |
| [Get Project Service Packages](actions/get-project-service-packages.md) | `GET projects/:projectID/service_packages/[:servicePackageID]` | [docs](https://api.jetbuilt.com/customers?shell--json#get-all-service-packages-in-your-project) |
| [Get Project Systems](actions/get-project-systems.md) | `GET projects/:projectId/systems` |  |
| [Get Projects](actions/get-projects.md) | `GET projects/:id` | [docs](https://api.jetbuilt.com/customers#projects) |
| [Get Proposals](actions/get-proposals.md) | `GET projects/:projectId/proposals` |  |
| [Get Purchase Order](actions/get-purchase-order.md) | `GET purchase_orders/[:id]` | [docs](https://api.jetbuilt.com/customers#get-a-purchase-order) |
| [Get Purchasing Sources](actions/get-purchasing-sources.md) | `GET purchasing/sources/:iD` | [docs](https://api.jetbuilt.com/customers#get-a-purchase-order) |
| [Get Service Case](actions/get-service-case.md) | `GET service_cases/[:serviceCaseId]` |  |
| [Get Sources](actions/get-sources.md) | `GET purchasing/sources/[:purchasingSourceId]` |  |
| [Get Tags](actions/get-tags.md) | `GET` |  |
| [Get User](actions/get-user.md) | `GET users/[:id]` |  |
| [Get Users](actions/get-users.md) | `GET users` |  |
| [Update a Project Item](actions/update-a-project-item.md) | `PUT projects/:projectId/items/:id` |  |
| [Update Client](actions/update-client.md) | `PATCH clients/:id` | [docs](https://api.jetbuilt.com/customers#update-a-client) |
| [Update Client Contact](actions/update-client-contact.md) | `PATCH clients/:client_id/contacts/:contact_id` | [docs](https://api.jetbuilt.com/customers#update-a-client-contact) |
| [Update Project](actions/update-project.md) | `PATCH projects/:projectId` |  |
