# <img src="https://images.mindcloud.co/apps/icons/v_1744240433900.png" alt="Viewpoint Spectrum logo" width="28" height="28"> Viewpoint Spectrum: Universal API

Web-based construction ERP solution with leading-edge tools

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/viewpointSpectrum/latest
- **Actions:** 14
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.viewpoint.com/resource-library/spectrum
- **Vendor API docs:** https://help.trimble.com/en/spectrum/spectrum/api-web-services/api-web-services

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Vendors](actions/list-vendors.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/viewpointSpectrum/latest/actions/list-vendors?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (14)

### Customers

| Action | Method | Description |
| --- | --- | --- |
| [Create Customer](actions/create-customer.md) | POST |  |
| [Get Customers](actions/get-customers.md) | GET |  |
| [List Customers](actions/list-customers.md) | GET |  |
| [Update Customer](actions/update-customer.md) | PUT |  |
| [Upsert Customer Bill-To](actions/upsert-customer-bill-to.md) | POST |  |

### Invoices

| Action | Method | Description |
| --- | --- | --- |
| [Create Customer Invoice](actions/create-customer-invoice.md) | POST |  |
| [Create Vendor Invoice](actions/create-vendor-invoice.md) | POST |  |
| [Create Work Orders](actions/create-work-orders.md) | POST |  |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Create Vendor Invoice Multi-Line](actions/create-vendor-invoice-multi-line.md) | POST |  |
| [Create AR Customer Invoice Multi-Line](actions/new-action1.md) | POST |  |

### Purchase Orders

| Action | Method | Description |
| --- | --- | --- |
| [Create Purchase Order](actions/create-purchase-order.md) | POST |  |

### Vendors

| Action | Method | Description |
| --- | --- | --- |
| [Create Vendor](actions/create-vendor.md) | POST |  |
| [List Vendors](actions/list-vendors.md) | GET |  |
| [Update Vendor](actions/update-vendor.md) | PUT |  |

