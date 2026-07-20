# <img src="https://images.mindcloud.co/apps/icons/u-on_1776461100467.png" alt="U-ON logo" width="28" height="28"> U-ON: Universal API

CRM for travel agencies, tour operators, and travel networks, with endpoints for tourists, leads, requests, payments, services, reminders, managers, directories, and webhooks.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/uON/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://u-on.travel/
- **Vendor API docs:** https://api.u-on.travel/doc

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Companies](actions/list-companies.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uON/latest/actions/list-companies?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Bill

| Action | Method | Description |
| --- | --- | --- |
| [Get Bill](actions/get-bill.md) | GET | Retrieves a bill record from U-ON. |
| [List Bills](actions/list-bills.md) | GET | Retrieves bill records stored in U-ON. |

### City

| Action | Method | Description |
| --- | --- | --- |
| [List Cities](actions/list-cities.md) | GET | Retrieves city records for a country in U-ON. |

### Company

| Action | Method | Description |
| --- | --- | --- |
| [List Companies](actions/list-companies.md) | GET | Retrieves company records stored in U-ON. |

### Company Office

| Action | Method | Description |
| --- | --- | --- |
| [List Company Offices](actions/list-company-offices.md) | GET | Retrieves company office records stored in U-ON. |

### Country

| Action | Method | Description |
| --- | --- | --- |
| [List Countries](actions/list-countries.md) | GET | Retrieves country records available in U-ON. |

### Currency

| Action | Method | Description |
| --- | --- | --- |
| [List Currencies](actions/list-currencies.md) | GET | Retrieves currency records available in U-ON. |

### Hotel

| Action | Method | Description |
| --- | --- | --- |
| [Get Hotel](actions/get-hotel.md) | GET | Retrieves a hotel record from U-ON. |
| [List Hotels](actions/list-hotels.md) | GET | Retrieves hotel records stored in U-ON. |

### Lead

| Action | Method | Description |
| --- | --- | --- |
| [Get Lead](actions/get-lead.md) | GET | Retrieves a lead record from U-ON. |
| [List Leads](actions/list-leads.md) | GET | Retrieves lead records stored in U-ON. |
| [List Leads by Client](actions/list-leads-by-client.md) | GET | Retrieves lead records for a U-ON client. |
| [List Updated Leads](actions/list-updated-leads.md) | GET | Retrieves leads updated in U-ON within a date range. |
| [Search Leads](actions/search-leads.md) | GET | Finds leads in U-ON by search criteria. |

### Lead Status

| Action | Method | Description |
| --- | --- | --- |
| [List Lead Statuses](actions/list-lead-statuses.md) | GET | Retrieves lead status records from U-ON. |

### Manager

| Action | Method | Description |
| --- | --- | --- |
| [Get Manager](actions/get-manager.md) | GET | Retrieves a manager record from U-ON. |
| [List Managers](actions/list-managers.md) | GET | Retrieves manager records stored in U-ON. |
| [List Managers by Office](actions/list-managers-by-office.md) | GET | Retrieves manager records for a U-ON office. |

### Payment

| Action | Method | Description |
| --- | --- | --- |
| [Get Payment](actions/get-payment.md) | GET | Retrieves a payment record from U-ON. |
| [List Payments](actions/list-payments.md) | GET | Retrieves payment records from U-ON within a date range. |

### Payment Status

| Action | Method | Description |
| --- | --- | --- |
| [List Payment Statuses](actions/list-payment-statuses.md) | GET | Retrieves payment status records from U-ON. |

### Request

| Action | Method | Description |
| --- | --- | --- |
| [Get Request](actions/get-request.md) | GET | Retrieves a request record from U-ON. |
| [List Closed Requests](actions/list-closed-requests.md) | GET | Retrieves closed requests in U-ON within a date range. |
| [List Requests](actions/list-requests.md) | GET | Retrieves request records stored in U-ON. |
| [List Requests by Client](actions/list-requests-by-client.md) | GET | Retrieves request records for a U-ON client. |
| [List Requests by Tourist](actions/list-requests-by-tourist.md) | GET | Retrieves request records for a U-ON tourist. |
| [List Updated Requests](actions/list-updated-requests.md) | GET | Retrieves requests updated in U-ON within a date range. |
| [Search Requests](actions/search-requests.md) | GET | Finds requests in U-ON by search criteria. |

### Request Status

| Action | Method | Description |
| --- | --- | --- |
| [List Request Statuses](actions/list-request-statuses.md) | GET | Retrieves request status records from U-ON. |

### Service

| Action | Method | Description |
| --- | --- | --- |
| [Search Services](actions/search-services.md) | GET | Finds services in U-ON by search criteria. |

### Service Type

| Action | Method | Description |
| --- | --- | --- |
| [List Service Types](actions/list-service-types.md) | GET | Retrieves service type records from U-ON. |

### Source

| Action | Method | Description |
| --- | --- | --- |
| [List Sources](actions/list-sources.md) | GET | Retrieves source records available in U-ON. |

### Supplier

| Action | Method | Description |
| --- | --- | --- |
| [Get Supplier](actions/get-supplier.md) | GET | Retrieves a supplier record from U-ON. |
| [List Suppliers](actions/list-suppliers.md) | GET | Retrieves supplier records stored in U-ON. |

### Tourist

| Action | Method | Description |
| --- | --- | --- |
| [Find Tourist by Phone](actions/find-tourist-by-phone.md) | GET | Finds a tourist in U-ON by phone number. |
| [Get Tourist](actions/get-tourist.md) | GET | Retrieves a tourist record from U-ON. |
| [List Tourists](actions/list-tourists.md) | GET | Retrieves tourist records stored in U-ON. |
| [List Updated Tourists](actions/list-updated-tourists.md) | GET | Retrieves tourists updated in U-ON within a date range. |
| [Search Tourists](actions/search-tourists.md) | GET | Finds tourists in U-ON by search criteria. |

### Travel Type

| Action | Method | Description |
| --- | --- | --- |
| [List Travel Types](actions/list-travel-types.md) | GET | Retrieves travel type records from U-ON. |

