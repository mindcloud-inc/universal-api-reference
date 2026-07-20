# <img src="https://images.mindcloud.co/apps/icons/images-4_1774035561553.jpeg" alt="MRPeasy logo" width="28" height="28"> MRPeasy: Universal API

MRPeasy manufacturing ERP app draft scaffolded for one-shot validation. Basic auth uses API key as username and API secret as password.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/mrpeasy/latest
- **Category:** Commerce / ERP
- **Actions:** 38
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.mrpeasy.com/
- **Vendor API docs:** https://www.mrpeasy.com/resources/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Customers](actions/list-customers.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mrpeasy/latest/actions/list-customers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (38)

### Bom

| Action | Method | Description |
| --- | --- | --- |
| [Create BOM](actions/create-bom.md) | POST | Creates a new BOM in MRPeasy. |
| [Delete BOM](actions/delete-bom.md) | DELETE | Deletes an existing BOM from MRPeasy. |
| [Get BOM](actions/get-bom.md) | GET | Retrieves a BOM from MRPeasy. |
| [List BOMs](actions/list-boms.md) | GET | Retrieves bills of materials from MRPeasy. |
| [Update BOM](actions/update-bom.md) | PUT | Updates an existing BOM in MRPeasy. |

### Customer

| Action | Method | Description |
| --- | --- | --- |
| [Create Customer](actions/create-customer.md) | POST | Creates a new customer in MRPeasy. |
| [Get Customer](actions/get-customer.md) | GET | Retrieves a customer from MRPeasy. |
| [List Customers](actions/list-customers.md) | GET | Retrieves customers from MRPeasy. |
| [Update Customer](actions/update-customer.md) | PUT | Updates an existing customer in MRPeasy. |

### Customer Order

| Action | Method | Description |
| --- | --- | --- |
| [Create Customer Order](actions/create-customer-order.md) | POST | Creates a new customer order in MRPeasy. |
| [Get Customer Order](actions/get-customer-order.md) | GET | Retrieves a customer order from MRPeasy. |
| [List Customer Orders](actions/list-customer-orders.md) | GET | Retrieves customer orders from MRPeasy. |
| [Update Customer Order](actions/update-customer-order.md) | PUT | Updates an existing customer order in MRPeasy. |

### Item

| Action | Method | Description |
| --- | --- | --- |
| [Create Item](actions/create-item.md) | POST | Creates a new stock item in MRPeasy. |
| [Delete Item](actions/delete-item.md) | DELETE | Deletes an existing stock item from MRPeasy. |
| [Get Item](actions/get-item.md) | GET | Retrieves a stock item from MRPeasy. |
| [List Items](actions/list-items.md) | GET | Retrieves stock items from MRPeasy. |
| [Update Item](actions/update-item.md) | PUT | Updates an existing stock item in MRPeasy. |

### Manufacturing Order

| Action | Method | Description |
| --- | --- | --- |
| [Create Manufacturing Order](actions/create-manufacturing-order.md) | POST | Creates a new manufacturing order in MRPeasy. |
| [Delete Manufacturing Order](actions/delete-manufacturing-order.md) | DELETE | Cancels an existing manufacturing order in MRPeasy. |
| [Get Manufacturing Order](actions/get-manufacturing-order.md) | GET | Retrieves a manufacturing order from MRPeasy. |
| [List Manufacturing Orders](actions/list-manufacturing-orders.md) | GET | Retrieves manufacturing orders from MRPeasy. |
| [Update Manufacturing Order](actions/update-manufacturing-order.md) | PUT | Updates an existing manufacturing order in MRPeasy. |

### Product Group

| Action | Method | Description |
| --- | --- | --- |
| [Get Product Group](actions/get-product-group.md) | GET | Retrieves a product group from MRPeasy. |
| [List Product Groups](actions/list-product-groups.md) | GET | Retrieves product groups from MRPeasy. |

### Purchase Order

| Action | Method | Description |
| --- | --- | --- |
| [Get Purchase Order](actions/get-purchase-order.md) | GET | Retrieves a purchase order from MRPeasy. |
| [List Purchase Orders](actions/list-purchase-orders.md) | GET | Retrieves purchase orders from MRPeasy. |

### Routing

| Action | Method | Description |
| --- | --- | --- |
| [Create Routing](actions/create-routing.md) | POST | Creates a new routing in MRPeasy. |
| [Delete Routing](actions/delete-routing.md) | DELETE | Deletes an existing routing from MRPeasy. |
| [Get Routing](actions/get-routing.md) | GET | Retrieves a routing from MRPeasy. |
| [List Routings](actions/list-routings.md) | GET | Retrieves routings from MRPeasy. |
| [Update Routing](actions/update-routing.md) | PUT | Updates an existing routing in MRPeasy. |

### Shipment

| Action | Method | Description |
| --- | --- | --- |
| [Get Shipment](actions/get-shipment.md) | GET | Retrieves a shipment from MRPeasy. |
| [List Shipments](actions/list-shipments.md) | GET | Retrieves shipments from MRPeasy. |

### Unit

| Action | Method | Description |
| --- | --- | --- |
| [Get Unit](actions/get-unit.md) | GET | Retrieves a unit from MRPeasy. |
| [List Units](actions/list-units.md) | GET | Retrieves units from MRPeasy. |

### Vendor

| Action | Method | Description |
| --- | --- | --- |
| [Get Vendor](actions/get-vendor.md) | GET | Retrieves a vendor from MRPeasy. |
| [List Vendors](actions/list-vendors.md) | GET | Retrieves vendors from MRPeasy. |

