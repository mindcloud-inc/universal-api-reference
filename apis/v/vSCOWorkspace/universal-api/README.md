# <img src="https://images.mindcloud.co/apps/icons/vsco-logo-png-seeklogo-432328_1773765428489.png" alt="VSCO Workspace logo" width="28" height="28"> VSCO Workspace: Universal API

Manage studio leads, jobs, galleries, orders, and payments

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/vSCOWorkspace/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.vsco.co/workspace
- **Vendor API docs:** https://workspace.vsco.co/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get My Studio](actions/get-my-studio.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vSCOWorkspace/latest/actions/get-my-studio?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in VSCO Workspace. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a contact from VSCO Workspace. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contacts from VSCO Workspace. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in VSCO Workspace. |

### Event

| Action | Method | Description |
| --- | --- | --- |
| [Create Event](actions/create-event.md) | POST | Creates a new event in VSCO Workspace. |
| [Get Event](actions/get-event.md) | GET | Retrieves an event from VSCO Workspace. |
| [List Events](actions/list-events.md) | GET | Retrieves events from VSCO Workspace. |
| [Update Event](actions/update-event.md) | PUT | Updates an existing event in VSCO Workspace. |

### File

| Action | Method | Description |
| --- | --- | --- |
| [Create File](actions/create-file.md) | POST | Creates a new file in VSCO Workspace. |
| [Get File](actions/get-file.md) | GET | Retrieves a file from VSCO Workspace. |
| [List Files](actions/list-files.md) | GET | Retrieves files from VSCO Workspace. |

### Gallery

| Action | Method | Description |
| --- | --- | --- |
| [Create Gallery](actions/create-gallery.md) | POST | Creates a new gallery in VSCO Workspace. |
| [Get Gallery](actions/get-gallery.md) | GET | Retrieves a gallery from VSCO Workspace. |
| [List Galleries](actions/list-galleries.md) | GET | Retrieves galleries from VSCO Workspace. |
| [Update Gallery](actions/update-gallery.md) | PUT | Updates an existing gallery in VSCO Workspace. |

### Job

| Action | Method | Description |
| --- | --- | --- |
| [Create Job](actions/create-job.md) | POST | Creates a new job in VSCO Workspace. |
| [Get Job](actions/get-job.md) | GET | Retrieves a job from VSCO Workspace. |
| [List Jobs](actions/list-jobs.md) | GET | Retrieves jobs from VSCO Workspace. |
| [Update Job](actions/update-job.md) | PUT | Updates an existing job in VSCO Workspace. |

### Order

| Action | Method | Description |
| --- | --- | --- |
| [Create Order for Job](actions/create-order-for-job.md) | POST | Creates a new order for a job in VSCO Workspace. |
| [Get Order](actions/get-order.md) | GET | Retrieves an order from VSCO Workspace. |
| [List Orders](actions/list-orders.md) | GET | Retrieves orders from VSCO Workspace. |
| [List Orders for Job](actions/list-orders-for-job.md) | GET | Retrieves orders for a job in VSCO Workspace. |
| [Update Order](actions/update-order.md) | PUT | Updates an existing order in VSCO Workspace. |

### Payment

| Action | Method | Description |
| --- | --- | --- |
| [Apply Payment to Order](actions/apply-payment-to-order.md) | POST | Applies a payment to an order in VSCO Workspace. |
| [Create Payment](actions/create-payment.md) | POST | Creates a new payment in VSCO Workspace. |
| [Get Payment](actions/get-payment.md) | GET | Retrieves a payment from VSCO Workspace. |
| [List Payments](actions/list-payments.md) | GET | Retrieves payments from VSCO Workspace. |
| [List Payments for Job](actions/list-payments-for-job.md) | GET | Retrieves payments for a job in VSCO Workspace. |

### Studio

| Action | Method | Description |
| --- | --- | --- |
| [Get My Studio](actions/get-my-studio.md) | GET | Retrieves your studio details from VSCO Workspace. |

