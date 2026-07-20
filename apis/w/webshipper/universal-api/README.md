# <img src="https://images.mindcloud.co/apps/icons/id9t7am-qn4-logos_1774462588107.png" alt="Webshipper logo" width="28" height="28"> Webshipper: Universal API

Manage shipping, orders, rates, and returns in Webshipper

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/webshipper/latest
- **Category:** Commerce / Supply Chain
- **Actions:** 50
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://webshipper.com
- **Vendor API docs:** https://docs.webshipper.io/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Order Channel Types](actions/list-order-channel-types.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/webshipper/latest/actions/list-order-channel-types?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (50)

### Activity

| Action | Method | Description |
| --- | --- | --- |
| [List Shipment Activities](actions/list-shipment-activities.md) | GET |  |

### Carrier

| Action | Method | Description |
| --- | --- | --- |
| [Get Carrier](actions/get-carrier.md) | GET | Retrieves a carrier from Webshipper. |
| [List Carriers](actions/list-carriers.md) | GET | Retrieves carriers from Webshipper. |

### Carrier Type

| Action | Method | Description |
| --- | --- | --- |
| [Get Carrier Type](actions/get-carrier-type.md) | GET | Retrieves a carrier type from Webshipper. |
| [List Carrier Types](actions/list-carrier-types.md) | GET | Retrieves carrier types from Webshipper. |

### Document

| Action | Method | Description |
| --- | --- | --- |
| [Get Document](actions/get-document.md) | GET | Retrieves a document from Webshipper. |
| [List Documents](actions/list-documents.md) | GET | Retrieves documents from Webshipper. |
| [List Order Documents](actions/list-order-documents.md) | GET |  |

### Event

| Action | Method | Description |
| --- | --- | --- |
| [List Shipment Events](actions/list-shipment-events.md) | GET |  |

### Label

| Action | Method | Description |
| --- | --- | --- |
| [Get Label](actions/get-label.md) | GET | Retrieves a label from Webshipper. |
| [List Labels](actions/list-labels.md) | GET | Retrieves labels from Webshipper. |

### Order

| Action | Method | Description |
| --- | --- | --- |
| [Get Order](actions/get-order.md) | GET | Retrieves an order from Webshipper. |
| [List Orders](actions/list-orders.md) | GET | Retrieves orders from Webshipper. |

### Order Channel

| Action | Method | Description |
| --- | --- | --- |
| [Get Order Channel](actions/get-order-channel.md) | GET | Retrieves an order channel from Webshipper. |
| [List Order Channels](actions/list-order-channels.md) | GET | Retrieves order channels from Webshipper. |

### Order Channel Type

| Action | Method | Description |
| --- | --- | --- |
| [List Order Channel Types](actions/list-order-channel-types.md) | GET | Retrieves order channel types from Webshipper. |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Create Order](actions/create-order.md) | POST | Creates an order in Webshipper. |
| [Create Shipping Rate](actions/create-shipping-rate.md) | POST | Creates a shipping rate in Webshipper. |
| [Delete Shipping Rate](actions/delete-shipping-rate.md) | DELETE | Deletes a shipping rate from Webshipper. |
| [Quote Carrier Services](actions/quote-carrier-services.md) | POST | Creates a carrier service quote in Webshipper. |
| [Quote Order Channel Rates](actions/quote-order-channel-rates.md) | POST | Creates an order channel rate quote in Webshipper. |
| [Update Order](actions/update-order.md) | PUT | Updates an order in Webshipper. |
| [Update Shipment](actions/update-shipment.md) | PUT |  |
| [Update Shipping Rate](actions/update-shipping-rate.md) | PUT | Updates a shipping rate in Webshipper. |

### Print Job

| Action | Method | Description |
| --- | --- | --- |
| [List Order Print Jobs](actions/list-order-print-jobs.md) | GET |  |

### Printer Client

| Action | Method | Description |
| --- | --- | --- |
| [List Printer Clients](actions/list-printer-clients.md) | GET | Retrieves printer clients from Webshipper. |

### Printer Job

| Action | Method | Description |
| --- | --- | --- |
| [List Printer Jobs](actions/list-printer-jobs.md) | GET | Retrieves printer jobs from Webshipper. |

### Report

| Action | Method | Description |
| --- | --- | --- |
| [Create Report](actions/create-report.md) | POST | Creates a report in Webshipper. |
| [Get Report](actions/get-report.md) | GET | Retrieves a report from Webshipper. |
| [List Reports](actions/list-reports.md) | GET | Retrieves reports from Webshipper. |

### Return

| Action | Method | Description |
| --- | --- | --- |
| [List Order Returns](actions/list-order-returns.md) | GET |  |

### Return Cause

| Action | Method | Description |
| --- | --- | --- |
| [Create Return Cause](actions/create-return-cause.md) | POST | Creates a return cause in Webshipper. |
| [Get Return Cause](actions/get-return-cause.md) | GET | Retrieves a return cause from Webshipper. |
| [List Return Causes](actions/list-return-causes.md) | GET | Retrieves return causes from Webshipper. |
| [Update Return Cause](actions/update-return-cause.md) | PUT | Updates a return cause in Webshipper. |

### Return Portal

| Action | Method | Description |
| --- | --- | --- |
| [Create Return Portal](actions/create-return-portal.md) | POST | Creates a return portal in Webshipper. |
| [Get Return Portal](actions/get-return-portal.md) | GET | Retrieves a return portal from Webshipper. |
| [List Return Portals](actions/list-return-portals.md) | GET | Retrieves return portals from Webshipper. |
| [Update Return Portal](actions/update-return-portal.md) | PUT | Updates a return portal in Webshipper. |

### Return Shipment

| Action | Method | Description |
| --- | --- | --- |
| [List Return Shipments](actions/list-return-shipments.md) | GET |  |

### Return Shipping Method

| Action | Method | Description |
| --- | --- | --- |
| [Create Return Shipping Method](actions/create-return-shipping-method.md) | POST | Creates a return shipping method in Webshipper. |
| [Get Return Shipping Method](actions/get-return-shipping-method.md) | GET | Retrieves a return shipping method from Webshipper. |
| [List Return Shipping Methods](actions/list-return-shipping-methods.md) | GET | Retrieves return shipping methods from Webshipper. |
| [Update Return Shipping Method](actions/update-return-shipping-method.md) | PUT | Updates a return shipping method in Webshipper. |

### Shipment

| Action | Method | Description |
| --- | --- | --- |
| [Create Shipment](actions/create-shipment.md) | POST | Creates a shipment in Webshipper. |
| [Get Shipment](actions/get-shipment.md) | GET | Retrieves a shipment from Webshipper. |
| [List Order Shipments](actions/list-order-shipments.md) | GET |  |
| [List Shipments](actions/list-shipments.md) | GET | Retrieves shipments from Webshipper. |

### Shipping Rate

| Action | Method | Description |
| --- | --- | --- |
| [Get Shipping Rate](actions/get-shipping-rate.md) | GET | Retrieves a shipping rate from Webshipper. |
| [List Shipping Rates](actions/list-shipping-rates.md) | GET | Retrieves shipping rates from Webshipper. |

