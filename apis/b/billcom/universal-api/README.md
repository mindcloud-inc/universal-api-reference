# <img src="https://images.mindcloud.co/apps/icons/billcom-icon_1782392943243.png" alt="BILL Payables & Receivables logo" width="28" height="28"> BILL Payables & Receivables: Universal API

The intelligent way to create and pay bills, send invoices, manage expenses, control budgets, and access the credit your business needs to grow—all on one platform.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/billcom/latest
- **Actions:** 19
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.bill.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Users](actions/list-users.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/billcom/latest/actions/list-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (19)

### Bill Approver

| Action | Method | Description |
| --- | --- | --- |
| [List Approvers Assigned to a Bill](actions/list-bill-approvers.md) | GET | Retrieves approvers assigned to a bill in Bill.com. |

### Bill Credit

| Action | Method | Description |
| --- | --- | --- |
| [List Bill Credits](actions/list-bill-credits.md) | GET | Retrieves bill credits from Bill.com. |

### Bills

| Action | Method | Description |
| --- | --- | --- |
| [Get Bill](actions/get-bill.md) | GET | Retrieves a bill from Bill.com. |
| [List Bills](actions/list-bills.md) | GET | Retrieves bills from Bill.com. |

### Chart Of Accounts

| Action | Method | Description |
| --- | --- | --- |
| [List Charts of Accounts](actions/list-charts-of-accounts.md) | GET | Retrieves chart of accounts from Bill.com. |

### Customers

| Action | Method | Description |
| --- | --- | --- |
| [List Customers](actions/list-customers.md) | GET | Retrieves customers from Bill.com. |

### Invoices

| Action | Method | Description |
| --- | --- | --- |
| [List Invoices](actions/list-invoices.md) | GET | Retrieves invoices from Bill.com. |

### Items

| Action | Method | Description |
| --- | --- | --- |
| [List Items](actions/list-items.md) | GET | Retrieves items from Bill.com. |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Approve Bill](actions/approve-bill.md) | POST | Approves a bill in Bill.com. |
| [Authenticate](actions/authenticate.md) | POST | Signs in to Bill.com and creates an API session. |
| [Create Record](actions/create-record.md) | POST | Creates a record in Bill.com. |
| [Update Record](actions/create-record-copy.md) | PUT | Updates a record in Bill.com. |

### Purchase Orders

| Action | Method | Description |
| --- | --- | --- |
| [List Purchase Orders](actions/list-purchase-orders.md) | GET | Retrieves purchase orders from Bill.com. |

### Sent Payment

| Action | Method | Description |
| --- | --- | --- |
| [List Sent Payments](actions/list-sent-payments.md) | GET | Retrieves sent payments from Bill.com. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [List Users](actions/list-users.md) | GET | Retrieves users from Bill.com. |

### Vendor Credits

| Action | Method | Description |
| --- | --- | --- |
| [List Vendor Credits](actions/list-vendor-credits.md) | GET | Retrieves vendor credits from Bill.com. |

### Vendors

| Action | Method | Description |
| --- | --- | --- |
| [Create Vendor](actions/create-vendor.md) | POST | Creates a vendor in Bill.com. |
| [List Vendors](actions/list-vendors.md) | GET | Retrieves vendors from Bill.com. |
| [Update Vendor](actions/update-vendor.md) | PUT | Updates a vendor in Bill.com. |

