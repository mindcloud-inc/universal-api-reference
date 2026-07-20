# <img src="https://images.mindcloud.co/apps/icons/ready-cloud-suite_1774871632627.png" alt="ReadyCloud Suite logo" width="28" height="28"> ReadyCloud Suite: Universal API

ReadyCloud Suite is a multichannel order and shipping operations platform with APIs for organizations, orders, boxes, tracking, items, notes, packaging, products, contacts, insurance, wallet subaccounts, events, and webhooks.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/readyCloudSuite/latest
- **Category:** Commerce
- **Actions:** 31
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.readycloud.com/
- **Vendor API docs:** https://www.readycloud.com/static/api-doc/v2/02-apireference-v2-00-intro.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Organizations](actions/list-organizations.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/readyCloudSuite/latest/actions/list-organizations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (31)

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in ReadyCloud Suite. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a contact from ReadyCloud Suite. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contacts from ReadyCloud Suite. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in ReadyCloud Suite. |

### Events

| Action | Method | Description |
| --- | --- | --- |
| [Get Tracking Detail](actions/get-tracking-detail.md) | GET | Retrieves a tracking entry from ReadyCloud Suite. |
| [List Tracking](actions/list-tracking.md) | GET | Retrieves tracking entries from ReadyCloud Suite. |

### Inventory Items

| Action | Method | Description |
| --- | --- | --- |
| [Create Packaging](actions/create-packaging.md) | POST | Creates a new packaging record in ReadyCloud Suite. |
| [Get Packaging](actions/get-packaging.md) | GET | Retrieves a packaging record from ReadyCloud Suite. |
| [List Packaging](actions/list-packaging.md) | GET | Retrieves packaging from ReadyCloud Suite. |
| [Update Packaging](actions/update-packaging.md) | PUT | Updates an existing packaging record in ReadyCloud Suite. |

### Notes

| Action | Method | Description |
| --- | --- | --- |
| [Create Note](actions/create-note.md) | POST | Creates a new note in ReadyCloud Suite. |
| [Get Note](actions/get-note.md) | GET | Retrieves a note from ReadyCloud Suite. |
| [List Notes](actions/list-notes.md) | GET | Retrieves notes from ReadyCloud Suite. |
| [Update Note](actions/update-note.md) | PUT | Updates an existing note in ReadyCloud Suite. |

### Organizations

| Action | Method | Description |
| --- | --- | --- |
| [List Organizations](actions/list-organizations.md) | GET | Retrieves organizations from ReadyCloud Suite. |

### Products

| Action | Method | Description |
| --- | --- | --- |
| [Create Product](actions/create-product.md) | POST | Creates a new product in ReadyCloud Suite. |
| [Get Product](actions/get-product.md) | GET | Retrieves a product from ReadyCloud Suite. |
| [List Products](actions/list-products.md) | GET | Retrieves products from ReadyCloud Suite. |
| [Update Product](actions/update-product.md) | PUT | Updates an existing product in ReadyCloud Suite. |

### Sales Orders

| Action | Method | Description |
| --- | --- | --- |
| [Create Order](actions/create-order.md) | POST | Creates a new order in ReadyCloud Suite. |
| [Get Order](actions/get-order.md) | GET | Retrieves an order from ReadyCloud Suite. |
| [List Orders](actions/list-orders.md) | GET | Retrieves orders from ReadyCloud Suite. |
| [Update Order](actions/update-order.md) | PUT | Updates an existing order in ReadyCloud Suite. |

### Shipment Items

| Action | Method | Description |
| --- | --- | --- |
| [Create Item](actions/create-item.md) | POST | Creates a new item in ReadyCloud Suite. |
| [Get Item](actions/get-item.md) | GET | Retrieves an item from ReadyCloud Suite. |
| [List Items](actions/list-items.md) | GET | Retrieves items from ReadyCloud Suite. |
| [Update Item](actions/update-item.md) | PUT | Updates an existing item in ReadyCloud Suite. |

### Shipments

| Action | Method | Description |
| --- | --- | --- |
| [Create Box](actions/create-box.md) | POST | Creates a new box in ReadyCloud Suite. |
| [Get Box](actions/get-box.md) | GET | Retrieves a box from ReadyCloud Suite. |
| [List Boxes](actions/list-boxes.md) | GET | Retrieves boxes from ReadyCloud Suite. |
| [Update Box](actions/update-box.md) | PUT | Updates an existing box in ReadyCloud Suite. |

