# <img src="https://images.mindcloud.co/apps/icons/vv_1772640224458.png" alt="Viewpoint Vista logo" width="28" height="28"> Viewpoint Vista: Universal API

Viewpoint Vista through the MindCloud Universal API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/viewpointVista/latest
- **Actions:** 63
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor API docs:** https://direct-api.xchange.trimble.com/reference/setup

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Action Instance](actions/get-action-instance.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/viewpointVista/latest/actions/get-action-instance?connectionId=$CONNECTION_ID&action_key_value=action-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (63)

### Accounts Payable

| Action | Method | Description |
| --- | --- | --- |
| [List AP Objects](actions/list-ap-objects.md) | GET | Represents data found in Viewpoint® Vista™ AP programs |
| [Search AP Objects](actions/search-ap-objects.md) | GET | Search objects found in the Viewpoint® Vista™ Accounts Payable (AP) programs. |

### Accounts Receivable

| Action | Method | Description |
| --- | --- | --- |
| [Create Customer Action](actions/create-customer-action.md) | POST |  |
| [List AR Objects](actions/list-ar-objects.md) | GET | Represents data found in Viewpoint® Vista™ AR programs |
| [Search AR Objects](actions/search-ar-objects.md) | GET | Search objects found in the Viewpoint® Vista™ Accounts Receivable (AR) programs. |
| [Update Customer Action](actions/update-customer-action.md) | PUT |  |
| [Update Vendor](actions/update-vendor.md) | PUT |  |

### Actions

| Action | Method | Description |
| --- | --- | --- |
| [Get Action Instance](actions/get-action-instance.md) | GET | Vista processes write operations asynchronously. This endpoint allows the integration to confirm whether a batch or time entry was… |

### Contracts

| Action | Method | Description |
| --- | --- | --- |
| [Create Contract](actions/create-contract.md) | POST | Create a contract |
| [Update Contract](actions/update-contract.md) | PUT | Update a contract |

### Document Management

| Action | Method | Description |
| --- | --- | --- |
| [List DM Objects](actions/list-dm-objects.md) | GET | Represents data found in Viewpoint® Vista™ DM programs. |
| [Search DM Objects](actions/search-dm-objects.md) | GET | Search objects found in the Viewpoint® Vista™ Document Management ( DM ) programs. |

### Equipment Management

| Action | Method | Description |
| --- | --- | --- |
| [List EM Objects](actions/list-em-objects.md) | GET | Represents data found in Viewpoint® Vista™ EM programs. |
| [Search EM Objects](actions/search-em-objects.md) | GET | Search data found in Viewpoint® Vista™ Equipment Management ( EM ) programs. |

### General Ledger

| Action | Method | Description |
| --- | --- | --- |
| [List GL Objects](actions/list-gl-objects.md) | GET | Represents data found in Viewpoint® Vista™ GL programs. |
| [Search GL Objects](actions/search-gl-objects.md) | GET | Search objects found in the Viewpoint® Vista™ General Ledger (GL) programs. |

### Headquarters

| Action | Method | Description |
| --- | --- | --- |
| [List HQ Objects](actions/list-hq-objects.md) | GET | Represents data found in Viewpoint® Vista™ HQ programs. |
| [Search HQ Objects](actions/search-hq-objects.md) | GET | Search objects found in Viewpoint® Vista™ Headquarters (HQ) programs. |

### Human Resources

| Action | Method | Description |
| --- | --- | --- |
| [List HR Objects](actions/list-hr-objects.md) | GET | Represents data found in Viewpoint® Vista™ HR programs. |
| [Search HR Objects](actions/search-hr-objects.md) | GET | Search objects found in Viewpoint® Vista™ Human Resources (HR) programs. |

### Inventory

| Action | Method | Description |
| --- | --- | --- |
| [List IN Objects](actions/list-in-objects.md) | GET | Represents data found in Viewpoint® Vista™ IN programs. |
| [Search IN Objects](actions/search-in-objects.md) | GET | Search objects found in Viewpoint® Vista™ Inventory (IN) programs. |

### Job Cost

| Action | Method | Description |
| --- | --- | --- |
| [List JC Objects](actions/list-jc-objects.md) | GET | Represents data found in Viewpoint® Vista™ JC programs. |
| [Search JC Objects](actions/search-jc-objects.md) | GET | Search objects found in Viewpoint® Vista™ Job Cost (JC) programs. |

### Jobs

| Action | Method | Description |
| --- | --- | --- |
| [Create Job](actions/create-job.md) | POST | Adds a Job based on a contract |
| [Update Job](actions/update-job.md) | PUT | Update a Job based on a contract |

### Material Sales

| Action | Method | Description |
| --- | --- | --- |
| [List MS Objects](actions/list-ms-objects.md) | GET | Represents data found in Viewpoint® Vista™ Material Sales V2 Direct API |
| [Search MS Objects](actions/search-ms-objects.md) | GET | Search objects found in Viewpoint® Vista™ Material Sales V2 Direct API |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Add Receipt Batch](actions/add-receipt-batch.md) | POST |  |
| [Add Receipt Batch Entry](actions/add-receipt-batch-entry.md) | POST |  |
| [Search Batches](actions/search-batches.md) | GET |  |

### Payroll

| Action | Method | Description |
| --- | --- | --- |
| [Add AR Contract Invoice](actions/add-ar-contract-invoice.md) | POST | Adds a Contract based invoice. |
| [Add Many Time Batch Entries](actions/add-many-payroll-timecard-entries.md) | POST | Add an array of time batch entries |
| [Add Non-Contract Invoice](actions/add-non-contract-invoice.md) | POST | Adds a Non-Contract based invoice. |
| [Get Timecard Batch by Ryvit ID](actions/get-timecard-batch-by-ryvit-id.md) | GET |  |
| [List PR Objects](actions/list-pr-objects.md) | GET | Represents data found in Viewpoint® Vista™ PR programs. |
| [Post Invoice Batch](actions/post-invoice-batch.md) | POST | Validate and post an AR Batch |
| [Search PR Objects](actions/search-pr-objects.md) | GET | Search objects found in Viewpoint® Vista™ Payroll (PR) programs. |
| [Upsert AR Invoice Batch](actions/upsert-ar-invoice-batch.md) | POST | Upsert Invoice Batch |
| [Upsert Invoice Batch](actions/upsert-invoice-batch.md) | POST | Upsert Invoice Batch |
| [Upsert Timecard Batch](actions/upsert-timecard-batch.md) | POST | Upsert TimeCard Batch |

### Pre-construction

| Action | Method | Description |
| --- | --- | --- |
| [List Potential Projects](actions/list-potential-projects.md) | GET | Represents Potential Project data in Viewpoint® Vista™. |
| [Search Potential Projects](actions/search-potential-projects.md) | GET | Search Potential Project objects in Viewpoint® Vista™. |

### Project Management

| Action | Method | Description |
| --- | --- | --- |
| [List PM Objects](actions/list-pm-objects.md) | GET | Represents data found in Viewpoint® Vista™ PM programs. |
| [Search PM Objects](actions/search-pm-objects.md) | GET | Search objects found in Viewpoint® Vista™ Project Management (PM) programs. |

### Purchase Order

| Action | Method | Description |
| --- | --- | --- |
| [List PO Objects](actions/list-po-objects.md) | GET | Represents data found in Viewpoint® Vista™ PO programs. |
| [Search PO Objects](actions/search-po-objects.md) | GET | Search objects found in Viewpoint® Vista™ Search (PO) programs. |

### Service Management

| Action | Method | Description |
| --- | --- | --- |
| [Add SM Customer](actions/add-sm-customer.md) | POST | Adds a new SM Customer Record. |
| [Add SM Work Order](actions/add-sm-work-order.md) | POST | Adds a Service Management work order header and automatically creates default Scope 1 in SMWorkOrderScope. |
| [Change SM Customer](actions/change-sm-customer.md) | POST | Changes an existing SM Customer |
| [Change SM Work Order](actions/change-sm-work-order.md) | POST | Changes an existing Work Order record. |
| [Get Customer by RyvitId](actions/get-customer-by-ryvit-id.md) | GET | Represents Info, Contacts and Notes tabs data found in Viewpoint® Vista™ SM Customer program. |
| [Get Customer by SMCo, CustGroup, Customer](actions/get-customer-by-sm-co-cust-group-customer.md) | GET | Represents Info, Contacts and Notes tabs data found in Viewpoint® Vista™ SM Customer program. |
| [Get Customer by SMCustomerID](actions/get-customer-by-sm-customer-id.md) | GET | Represents Info, Contacts and Notes tabs data found in Viewpoint® Vista™ SM Customer program. |
| [Get Service Site by SMServiceSiteID](actions/get-service-site-by-sm-service-site-id.md) | GET | Represents Info, Serviceable Items, Contacts and Notes tabs data found in Viewpoint® Vista™ SM Service Site program. |
| [List SM Objects](actions/list-sm-objects.md) | GET | Represents data found in Viewpoint® Vista™ SM programs. |
| [Search SM Objects](actions/search-sm-objects.md) | GET | Search data found in Viewpoint® Vista™ Service Management ( SM ) programs. |

### Subcontract Ledger

| Action | Method | Description |
| --- | --- | --- |
| [List SL Objects](actions/list-sl-objects.md) | GET | Represents data found in Viewpoint® Vista™ SL programs. |
| [Search SL Objects](actions/search-sl-objects.md) | GET | Search objects found in Viewpoint® Vista™ Subcontract Ledger (SL) programs. |

### Transactions

| Action | Method | Description |
| --- | --- | --- |
| [Search Batch Entries](actions/search-batch-entries.md) | GET |  |
| [Search Transactions](actions/search-transactions.md) | GET |  |

### User Defined Tables

| Action | Method | Description |
| --- | --- | --- |
| [List UD Objects](actions/list-ud-objects.md) | GET | Represents data found in Viewpoint® Vista™ UD programs. |
| [Search UD Objects](actions/search-ud-objects.md) | GET | Search objects found in Viewpoint® Vista™ User Defined Tables (UD) programs. |

