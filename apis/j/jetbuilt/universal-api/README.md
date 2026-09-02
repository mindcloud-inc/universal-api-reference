# <img src="https://images.mindcloud.co/apps/icons/jetbuilt-icon_1782393779179.png" alt="Jetbuilt logo" width="28" height="28"> Jetbuilt: Universal API

Jetbuilt through the MindCloud Universal API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/jetbuilt/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 42
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://jetbuilt.com/
- **Vendor API docs:** https://api.jetbuilt.com/customers#introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Project Items](actions/get-project-items.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jetbuilt/latest/actions/get-project-items?connectionId=$CONNECTION_ID&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (42)

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Update Client Contact](actions/update-client-contact.md) | PUT | Update a specified contact for a specified client. |

### Inventories

| Action | Method | Description |
| --- | --- | --- |
| [Get All Stock Products](actions/get-all-stock-products.md) | GET | Retrieves all of your stock products. |

### Items

| Action | Method | Description |
| --- | --- | --- |
| [Get All Stock Items](actions/get-all-stock-items.md) | GET | Retrieves all of your stock items. |
| [Get Project Items](actions/get-project-items.md) | GET |  |
| [Get Project Service Packages](actions/get-project-service-packages.md) | GET | Retrieve all of the service_packages attached to a given project. |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Create a Product](actions/create-a-product.md) | POST |  |
| [Create a Project Revision](actions/create-a-project-revision.md) | POST |  |
| [Create Client](actions/create-client.md) | POST |  |
| [Create Client Contact](actions/create-client-contact.md) | POST |  |
| [Create Project](actions/create-project.md) | POST |  |
| [Create Project Item](actions/create-project-item.md) | POST |  |
| [Create Project System](actions/create-project-system.md) | GET |  |
| [Get a Product](actions/get-a-product.md) | GET |  |
| [Get All Products](actions/get-all-products.md) | GET |  |
| [Get Client](actions/get-client.md) | GET | Get a Client |
| [Get Client Contacts](actions/get-client-contacts.md) | GET |  |
| [Get All Clients](actions/get-clients.md) | GET | Get a Clients |
| [Get Company](actions/get-company.md) | GET |  |
| [Get Market Segment](actions/get-market-segment.md) | GET |  |
| [Get Project Factors](actions/get-project-factors.md) | GET |  |
| [Get Project Systems](actions/get-project-systems.md) | GET |  |
| [Get Proposals](actions/get-proposals.md) | GET |  |
| [Get Sources](actions/get-sources.md) | GET |  |
| [Get Tags](actions/get-tags.md) | GET | Retrieves the tags for a specific project. |
| [Get Users](actions/get-users.md) | GET |  |
| [Update a Project Item](actions/update-a-project-item.md) | PUT |  |
| [Update Client](actions/update-client.md) | PUT |  |
| [Update Project](actions/update-project.md) | PATCH |  |

### Products

| Action | Method | Description |
| --- | --- | --- |
| [Get a product for a vendor](actions/get-a-product-for-a-vendor.md) | GET | This endpoint retrieves a product for a vendor by ID. |

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [Get a Room](actions/get-a-room.md) | GET | Retrieve the details of an individual project room. Equipment and labor totals (cost & price). Line items in this room. Project factors,… |
| [Get All Rooms](actions/get-all-rooms.md) | GET |  |
| [Get Project Options](actions/get-project-options.md) | GET |  |
| [Get Projects](actions/get-projects.md) | GET |  |

### Purchase Orders

| Action | Method | Description |
| --- | --- | --- |
| [Get Project Purchasing](actions/get-project-purchasing.md) | GET |  |
| [Get Purchase Order](actions/get-purchase-order.md) | GET |  |

### Services

| Action | Method | Description |
| --- | --- | --- |
| [Get Service Case](actions/get-service-case.md) | GET |  |

### Timesheets

| Action | Method | Description |
| --- | --- | --- |
| [Get Labor Presets](actions/get-labor-presets.md) | GET | Retrieves all labor presets for your company. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get User](actions/get-user.md) | GET | Get an User by id |

### Vendors

| Action | Method | Description |
| --- | --- | --- |
| [Get a Vendor](actions/get-a-vendor.md) | GET | This endpoint retrieves a vendor by ID. |
| [Get All Products for a Vendor](actions/get-all-products-for-a-vendor.md) | GET | Retrieves all products with your connected pricing for a specified vendor. |
| [List Vendors](actions/get-all-vendors.md) | GET |  |
| [Get Purchasing Sources](actions/get-purchasing-sources.md) | GET |  |

