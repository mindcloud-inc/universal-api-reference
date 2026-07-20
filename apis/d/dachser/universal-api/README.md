# <img src="https://images.mindcloud.co/apps/icons/captura-de-tela-2026-04-20-as-11_1776695421011.png" alt="Dachser logo" width="28" height="28"> Dachser: Universal API

Connect to DACHSER's REST/JSON logistics APIs for transport orders, shipment tracking, proofs of delivery, freight costs, labels, routing, SSCCs, warehouse delivery documents, delivery order statuses, incoming goods documents, and stock.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/dachser/latest
- **Category:** Commerce / Supply Chain
- **Actions:** 19
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.dachser.com/
- **Vendor API docs:** https://api-portal.dachser.com/bi.b2b.portal/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Stock](actions/get-stock.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dachser/latest/actions/get-stock?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (19)

### Charges

| Action | Method | Description |
| --- | --- | --- |
| [Get Freight Costs](actions/get-freight-costs.md) | GET | Retrieves freight costs for a consignment from Dachser. |

### Documents

| Action | Method | Description |
| --- | --- | --- |
| [Download Transfer Lists](actions/download-transfer-lists.md) | GET | Downloads transfer lists for a specific date from Dachser. |
| [Get Delivery Notes](actions/get-delivery-notes.md) | GET | Retrieves delivery notes from Dachser by reference or date. |
| [Get Incoming Goods Documents](actions/get-incoming-goods-documents.md) | GET | Retrieves incoming goods documents from Dachser. |
| [Get Proofs Of Delivery](actions/get-proofs-of-delivery.md) | GET | Retrieves proofs of delivery from Dachser. |
| [Get Transport Order Labels](actions/get-transport-order-labels.md) | GET | Retrieves labels for an existing transport order in Dachser. |

### Inventory Levels

| Action | Method | Description |
| --- | --- | --- |
| [Get Stock](actions/get-stock.md) | GET | Retrieves stock records from Dachser by article or warehouse. |

### Labels

| Action | Method | Description |
| --- | --- | --- |
| [Create Labels](actions/create-labels.md) | POST | Creates shipping labels for a shipment in Dachser. |

### Orders

| Action | Method | Description |
| --- | --- | --- |
| [Create Transport Order](actions/create-transport-order.md) | POST | Creates a new transport order in Dachser. |
| [Delete Transport Order](actions/delete-transport-order.md) | DELETE | Deletes an existing transport order from Dachser. |
| [Get Delivery Order Status](actions/get-delivery-order-status.md) | GET | Retrieves delivery order status from Dachser. |
| [List Transport Orders](actions/list-transport-orders.md) | GET | Retrieves transport orders from Dachser within a date range. |
| [List Transport Orders By Basket](actions/list-transport-orders-by-basket.md) | GET | Retrieves transport orders from a specific Dachser basket. |
| [Send Transport Order](actions/send-transport-order.md) | PUT | Sends an existing transport order to Dachser TMS. |

### Quotes

| Action | Method | Description |
| --- | --- | --- |
| [Create Quotation](actions/create-quotation.md) | POST | Creates a new quotation in Dachser. |

### Routing

| Action | Method | Description |
| --- | --- | --- |
| [Get Routing](actions/get-routing.md) | GET | Retrieves routing details for a destination from Dachser. |

### Shipments

| Action | Method | Description |
| --- | --- | --- |
| [Get Shipment History](actions/get-shipment-history.md) | GET | Retrieves shipment history details from Dachser. |
| [Get Shipment Status](actions/get-shipment-status.md) | GET | Retrieves shipment status details from Dachser. |

### Sscc Codes

| Action | Method | Description |
| --- | --- | --- |
| [Create SSCC Codes](actions/create-sscc-codes.md) | POST | Creates SSCC codes for shipments in Dachser. |

