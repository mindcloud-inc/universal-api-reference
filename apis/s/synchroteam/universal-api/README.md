# <img src="https://images.mindcloud.co/apps/icons/synchroteam_1775243676462.png" alt="Synchroteam logo" width="28" height="28"> Synchroteam: Universal API

Synchroteam is a field service management (FSM) platform. This app integrates with the Synchroteam API to manage jobs, customers, sites, equipment, parts, invoices, and users.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/synchroteam/latest
- **Category:** Support / Field Service
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.synchroteam.com
- **Vendor API docs:** https://api.synchroteam.com/v2/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Customers](actions/list-customers.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/synchroteam/latest/actions/list-customers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Activity

| Action | Method | Description |
| --- | --- | --- |
| [Search Activities](actions/search-activities.md) | GET | Finds activities in Synchroteam using supported search filters. |

### Activity Type

| Action | Method | Description |
| --- | --- | --- |
| [Search Activity Types](actions/search-activity-types.md) | GET | Finds activity types in Synchroteam using supported search filters. |
| [Send Activity Type](actions/send-activity-type.md) | PUT | Creates or updates an activity type in Synchroteam. |

### Attachment

| Action | Method | Description |
| --- | --- | --- |
| [Send Attachment](actions/send-attachment.md) | POST | Creates an attachment in Synchroteam for a job or customer. |

### Customer

| Action | Method | Description |
| --- | --- | --- |
| [Get Customer](actions/get-customer.md) | GET | Retrieves a customer from Synchroteam by supported identifier. |
| [List Customers](actions/list-customers.md) | GET | Retrieves customers from Synchroteam, optionally filtered by change date. |
| [Send Customer](actions/send-customer.md) | PUT | Creates or updates a customer in Synchroteam. |

### Equipment

| Action | Method | Description |
| --- | --- | --- |
| [Get Equipment](actions/get-equipment.md) | GET | Retrieves equipment from Synchroteam by supported identifier. |
| [Send Equipment](actions/send-equipment.md) | PUT | Creates or updates equipment in Synchroteam. |

### Inventory Quantity

| Action | Method | Description |
| --- | --- | --- |
| [Initialize Quantities](actions/initialize-quantities.md) | PUT | Initializes part quantities in Synchroteam stock depots. |

### Invoice

| Action | Method | Description |
| --- | --- | --- |
| [List Invoices and Quotations](actions/list-invoices-and-quotations.md) | GET | Retrieves invoices and quotations from Synchroteam using supported filters. |
| [Send Invoice or Quotation](actions/send-invoice-or-quotation.md) | PUT | Creates or updates an invoice or quotation in Synchroteam. |

### Job

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Job](actions/cancel-job.md) | PUT | Cancels a job in Synchroteam by supported identifier. |
| [Get Job Detail](actions/get-job-detail.md) | GET | Retrieves a job from Synchroteam by supported identifier. |
| [Search Jobs](actions/search-jobs.md) | GET | Finds jobs in Synchroteam using supported search filters. |
| [Send Job](actions/send-job.md) | PUT | Creates or updates a job in Synchroteam. |
| [Validate Job](actions/validate-job.md) | PUT | Validates a job in Synchroteam by supported identifier. |

### Job Photo

| Action | Method | Description |
| --- | --- | --- |
| [Get Job Photos](actions/get-job-photos.md) | GET | Retrieves photos for a job from Synchroteam. |

### Part

| Action | Method | Description |
| --- | --- | --- |
| [Get Part Detail](actions/get-part-detail.md) | GET | Retrieves a part from Synchroteam by supported identifier. |
| [Send Part](actions/send-part.md) | PUT | Creates or updates a part in Synchroteam. |
| [Update Parts Pricing](actions/update-parts-pricing.md) | PUT | Updates pricing for parts in Synchroteam. |

### Shared Block

| Action | Method | Description |
| --- | --- | --- |
| [List Shared Blocks](actions/list-shared-blocks.md) | GET | Retrieves a list of shared blocks from Synchroteam. |

### Site

| Action | Method | Description |
| --- | --- | --- |
| [Get Site](actions/get-site.md) | GET | Retrieves a site from Synchroteam by supported identifier. |
| [List Sites by Customer ID](actions/list-sites-by-customer-id.md) | GET | Retrieves sites from Synchroteam for a specific customer ID. |
| [Send Site](actions/send-site.md) | PUT | Creates or updates a site in Synchroteam. |

### Stock Request

| Action | Method | Description |
| --- | --- | --- |
| [Complete Replenishment](actions/complete-replenishment.md) | PUT | Completes a replenishment request in Synchroteam. |
| [Search Replenishment Requests](actions/search-replenishment-requests.md) | GET | Finds replenishment requests in Synchroteam using supported filters. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get User Detail](actions/get-user-detail.md) | GET | Retrieves a user from Synchroteam by supported identifier. |
| [Search Users](actions/search-users.md) | GET | Finds users in Synchroteam using supported search filters. |
| [Send User](actions/send-user.md) | PUT | Creates or updates a user in Synchroteam. |

