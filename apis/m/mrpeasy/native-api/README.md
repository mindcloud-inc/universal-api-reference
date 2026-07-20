# MRPeasy: Native API Reference

A consolidated summary of MRPeasy's API configuration and 38 documented operations, with links to official documentation.

- **Official docs:** https://www.mrpeasy.com/resources/api/
- **API base URL:** `https://api.mrpeasy.com/rest/v1`

## Authentication

### API Key + Secret

Enter your MRPeasy API key in the username field and your MRPeasy API secret in the password field.

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

[Official authentication documentation](https://www.mrpeasy.com/resources/api/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (38 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create BOM](actions/create-bom.md) | `POST /boms` | [docs](https://www.mrpeasy.com/resources/api/) |
| [Create Customer](actions/create-customer.md) | `POST /customers` | [docs](https://www.mrpeasy.com/resources/api/) |
| [Create Customer Order](actions/create-customer-order.md) | `POST /customer-orders` | [docs](https://www.mrpeasy.com/resources/api/) |
| [Create Item](actions/create-item.md) | `POST /items` | [docs](https://www.mrpeasy.com/resources/api/) |
| [Create Manufacturing Order](actions/create-manufacturing-order.md) | `POST /manufacturing-orders` | [docs](https://www.mrpeasy.com/resources/api/) |
| [Create Routing](actions/create-routing.md) | `POST /routings` | [docs](https://www.mrpeasy.com/resources/api/) |
| [Delete BOM](actions/delete-bom.md) | `DELETE /boms/{{bomId}}` | [docs](https://www.mrpeasy.com/resources/api/) |
| [Delete Item](actions/delete-item.md) | `DELETE /items/{{articleId}}` | [docs](https://www.mrpeasy.com/resources/api/) |
| [Delete Manufacturing Order](actions/delete-manufacturing-order.md) | `DELETE /manufacturing-orders/{{manOrdId}}` | [docs](https://www.mrpeasy.com/resources/api/) |
| [Delete Routing](actions/delete-routing.md) | `DELETE /routings/{{routingId}}` | [docs](https://www.mrpeasy.com/resources/api/) |
| [Get BOM](actions/get-bom.md) | `GET /boms/{{bomId}}` | [docs](https://www.mrpeasy.com/resources/api/) |
| [Get Customer](actions/get-customer.md) | `GET /customers/{{customerId}}` | [docs](https://www.mrpeasy.com/resources/api/) |
| [Get Customer Order](actions/get-customer-order.md) | `GET /customer-orders/{{custOrdId}}` | [docs](https://www.mrpeasy.com/resources/api/) |
| [Get Item](actions/get-item.md) | `GET /items/{{articleId}}` | [docs](https://www.mrpeasy.com/resources/api/) |
| [Get Manufacturing Order](actions/get-manufacturing-order.md) | `GET /manufacturing-orders/{{manOrdId}}` | [docs](https://www.mrpeasy.com/resources/api/) |
| [Get Product Group](actions/get-product-group.md) | `GET /product-groups/{{groupId}}` | [docs](https://www.mrpeasy.com/resources/api/) |
| [Get Purchase Order](actions/get-purchase-order.md) | `GET /purchase-orders/{{purOrdId}}` | [docs](https://www.mrpeasy.com/resources/api/) |
| [Get Routing](actions/get-routing.md) | `GET /routings/{{routingId}}` | [docs](https://www.mrpeasy.com/resources/api/) |
| [Get Shipment](actions/get-shipment.md) | `GET /shipments/{{shipmentId}}` | [docs](https://www.mrpeasy.com/resources/api/) |
| [Get Unit](actions/get-unit.md) | `GET /units/{{unitId}}` | [docs](https://www.mrpeasy.com/resources/api/) |
| [Get Vendor](actions/get-vendor.md) | `GET /vendors/{{vendorId}}` | [docs](https://www.mrpeasy.com/resources/api/) |
| [List BOMs](actions/list-boms.md) | `GET /boms` | [docs](https://www.mrpeasy.com/resources/api/) |
| [List Customer Orders](actions/list-customer-orders.md) | `GET /customer-orders` | [docs](https://www.mrpeasy.com/resources/api/) |
| [List Customers](actions/list-customers.md) | `GET /customers` | [docs](https://www.mrpeasy.com/resources/api/) |
| [List Items](actions/list-items.md) | `GET /items` | [docs](https://www.mrpeasy.com/resources/api/) |
| [List Manufacturing Orders](actions/list-manufacturing-orders.md) | `GET /manufacturing-orders` | [docs](https://www.mrpeasy.com/resources/api/) |
| [List Product Groups](actions/list-product-groups.md) | `GET /product-groups` | [docs](https://www.mrpeasy.com/resources/api/) |
| [List Purchase Orders](actions/list-purchase-orders.md) | `GET /purchase-orders` | [docs](https://www.mrpeasy.com/resources/api/) |
| [List Routings](actions/list-routings.md) | `GET /routings` | [docs](https://www.mrpeasy.com/resources/api/) |
| [List Shipments](actions/list-shipments.md) | `GET /shipments` | [docs](https://www.mrpeasy.com/resources/api/) |
| [List Units](actions/list-units.md) | `GET /units` | [docs](https://www.mrpeasy.com/resources/api/) |
| [List Vendors](actions/list-vendors.md) | `GET /vendors` | [docs](https://www.mrpeasy.com/resources/api/) |
| [Update BOM](actions/update-bom.md) | `PUT /boms/{{bomId}}` | [docs](https://www.mrpeasy.com/resources/api/) |
| [Update Customer](actions/update-customer.md) | `PUT /customers/{{customerId}}` | [docs](https://www.mrpeasy.com/resources/api/) |
| [Update Customer Order](actions/update-customer-order.md) | `PUT /customer-orders/{{custOrdId}}` | [docs](https://www.mrpeasy.com/resources/api/) |
| [Update Item](actions/update-item.md) | `PUT /items/{{articleId}}` | [docs](https://www.mrpeasy.com/resources/api/) |
| [Update Manufacturing Order](actions/update-manufacturing-order.md) | `PUT /manufacturing-orders/{{manOrdId}}` | [docs](https://www.mrpeasy.com/resources/api/) |
| [Update Routing](actions/update-routing.md) | `PUT /routings/{{routingId}}` | [docs](https://www.mrpeasy.com/resources/api/) |
