# <img src="https://images.mindcloud.co/apps/icons/aspire_1777387133843.png" alt="Aspire logo" width="28" height="28"> Aspire: Universal API

Field service software to drive growth

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/aspire/latest
- **Category:** Human Resources / HRIS
- **Actions:** 153
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.youraspire.com/
- **Vendor API docs:** https://guide.youraspire.com/apidocs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get API Version](actions/get-api-version.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aspire/latest/actions/get-api-version?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (153)

### Activity

| Action | Method | Description |
| --- | --- | --- |
| [List Activities](actions/list-activities.md) | GET |  |
| [List Activity Categories](actions/list-activity-categories.md) | GET | Activity categories allow you to provide a further descriptive breakdown for issues and tasks (i.e., for an issue, the category could be… |
| [List Activity Comment Histories](actions/list-activity-comment-histories.md) | GET | Retrieves activity comment histories from your Aspire account. |
| [List Activity Contacts](actions/list-activity-contacts.md) | GET | Retrieves activity contacts from your Aspire account. |

### Addresses

| Action | Method | Description |
| --- | --- | --- |
| [List Addresses](actions/list-addresses.md) | GET |  |

### Api Version

| Action | Method | Description |
| --- | --- | --- |
| [Get API Version](actions/get-api-version.md) | GET | Retrieves the current API version from Aspire. |

### Auth

| Action | Method | Description |
| --- | --- | --- |
| [Get Workers Comps](actions/get-contact-types.md) | GET | Retrieve a list of information related to workers' compensation. |
| [List Contact Types](actions/list-contact-types.md) | GET | Retrieve a list of contact types for the authenticated account. |

### Authentication

| Action | Method | Description |
| --- | --- | --- |
| [Authenticate](actions/authenticate.md) | GET |  |
| [Refresh Authorization Token](actions/refresh-authorization-token.md) | GET | Refreshes the current authorization token in Aspire. |

### Bank Feed Accounts

| Action | Method | Description |
| --- | --- | --- |
| [List Bank Deposits](actions/list-bank-deposits.md) | GET |  |

### Catalog Item

| Action | Method | Description |
| --- | --- | --- |
| [Create Catalog Item](actions/create-catalog-item.md) | POST | Creates a new catalog item in your Aspire account. |
| [Update Catalog Item](actions/update-catalog-item.md) | PUT | Updates an existing catalog item in your Aspire account. |

### Catalogs

| Action | Method | Description |
| --- | --- | --- |
| [List Catalog Item Categories](actions/list-catalog-item-categories.md) | GET |  |
| [List Catalog Items](actions/list-catalog-items.md) | GET |  |

### Certification

| Action | Method | Description |
| --- | --- | --- |
| [List Certification Types](actions/list-certification-types.md) | GET | Retrieves certification types from your Aspire account. |
| [List Certifications](actions/list-certifications.md) | GET | Retrieves certifications from your Aspire account. |

### Clock Time

| Action | Method | Description |
| --- | --- | --- |
| [Create Clock Time](actions/create-clock-time.md) | POST |  |
| [List Clock Times](actions/list-clock-times.md) | GET |  |

### Companies

| Action | Method | Description |
| --- | --- | --- |
| [Create Company](actions/create-companies.md) | POST | Add a new company. |
| [List Branches](actions/list-branches.md) | GET | Retrieve a list of information related to branches in an organization. |
| [List Companies](actions/list-companies.md) | GET | Retrieves a list of commercial or enterprise businesses associated with a contact. |
| [List Divisions](actions/list-divisions.md) | GET | Retrieve a list of information related to a division or divisions. |
| [List Tax Jurisdictions](actions/list-tax-jurisdictions.md) | GET | Retrieve a list of tax jurisdictions. |
| [Update Company](actions/update-company.md) | PUT | Updates an existing company in your Aspire account. |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Add a new contact. |
| [List Contacts](actions/list-contacts.md) | GET |  |
| [List Employee Incidents](actions/list-employee-incidents.md) | GET |  |
| [Update Contact](actions/update-contact.md) | PUT | Update an existing contact record. |

### Custom Fields

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact Custom Field](actions/create-contact-custom-field.md) | POST | Creates a new contact custom field in your Aspire account. |
| [List Contact Custom Field Definitions](actions/list-contact-custom-field-definitions.md) | GET | Retrieves contact custom field definitions from your Aspire account. |
| [List Contact Custom Fields](actions/list-contact-custom-fields.md) | GET | Retrieves contact custom fields from your Aspire account. |
| [Update Contact Custom Field](actions/update-contact-custom-field.md) | PUT | Updates an existing contact custom field in your Aspire account. |

### Division

| Action | Method | Description |
| --- | --- | --- |
| [List Division Integration Codes](actions/list-division-integration-codes.md) | GET | Retrieves division integration codes from your Aspire account. |

### Employee Incident

| Action | Method | Description |
| --- | --- | --- |
| [List Employee Incident Types](actions/list-employee-incident-types.md) | GET | Retrieves employee incident types from your Aspire account. |

### Employees

| Action | Method | Description |
| --- | --- | --- |
| [List Pay Schedules](actions/list-pay-schedules.md) | GET | Retrieves takeoff groups from your Aspire account. |
| [List Roles](actions/list-roles.md) | GET | Updates an existing pay code in your Aspire account. |
| [List Users](actions/list-users.md) | GET | Creates a new pay code in your Aspire account. |
| [Update User](actions/update-user.md) | PUT | Modify an existing users Branch Access and Role. Optionally specify a new Password. |

### Equipment

| Action | Method | Description |
| --- | --- | --- |
| [Create Equipment Reading Log](actions/create-equipment-reading-log.md) | POST | Creates a new equipment reading log in your Aspire account. |
| [List Equipment Classes](actions/list-equipment-classes.md) | GET | Retrieves equipment classes from your Aspire account. |
| [List Equipment Disposal Reasons](actions/list-equipment-disposal-reasons.md) | GET | Retrieves equipment disposal reasons from your Aspire account. |
| [List Equipment Manufacturers](actions/list-equipment-manufacturers.md) | GET | Retrieves equipment manufacturers from your Aspire account. |
| [List Equipment Model Service Schedules](actions/list-equipment-model-service-schedules.md) | GET | Retrieves equipment model service schedules from your Aspire account. |
| [List Equipment Models](actions/list-equipment-models.md) | GET | Retrieves equipment models from your Aspire account. |
| [List Equipment Reading Logs](actions/list-equipment-reading-logs.md) | GET | Retrieves equipment reading logs from your Aspire account. |
| [List Equipment Requested Services](actions/list-equipment-requested-services.md) | GET | Retrieves equipment requested services from your Aspire account. |
| [List Equipment Service Logs](actions/list-equipment-service-logs.md) | GET | Retrieves equipment service logs from your Aspire account. |
| [List Equipment Service Tags](actions/list-equipment-service-tags.md) | GET | Retrieves equipment service tags from your Aspire account. |
| [List Equipment Sizes](actions/list-equipment-sizes.md) | GET | Retrieves equipment sizes from your Aspire account. |
| [List Equipments](actions/list-equipments.md) | GET |  |
| [Update Equipment Reading Log](actions/update-equipment-reading-log.md) | PUT | Updates an existing equipment reading log in your Aspire account. |

### Expense Reports

| Action | Method | Description |
| --- | --- | --- |
| [Approve Receipt](actions/approve-receipt.md) | POST | Approves an existing Aspire receipt and can optionally receive it at the same time. This is the only post-create update path for a receipt.… |
| [Create Receipt](actions/create-receipt.md) | POST | Creates a new receipt in your Aspire account. |
| [List Receipts](actions/list-receipts.md) | GET | Lists Aspire receipts using the available OData query parameters. Use this to find existing receipts and inspect fields such as status,… |
| [Receive Receipt](actions/receive-receipt.md) | POST | Marks an existing Aspire receipt as received. This action accepts the receipt identifier only and does not perform receipt-level edits. It… |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Get Attachment File Data](actions/get-attachment-file-data.md) | GET | Retrieve a list of information related to an attached file, including the File Data encoded as a base 64 string. |
| [List Attachment Types](actions/list-attachment-types.md) | GET |  |
| [List Attachments](actions/list-attachments.md) | GET |  |
| [Post Attachment](actions/post-attachment.md) | POST |  |

### Invoice Tax

| Action | Method | Description |
| --- | --- | --- |
| [List Invoice Taxes](actions/list-invoice-taxes.md) | GET | Retrieves invoice taxes from your Aspire account. |

### Invoices

| Action | Method | Description |
| --- | --- | --- |
| [List Invoice Revenues](actions/get-invoice-revenue.md) | GET | Retrieves pay codes from your Aspire account. |
| [List Invoice Batches](actions/list-invoice-batches.md) | GET | Retrieves invoice batches from your Aspire account. |
| [List Invoices](actions/list-invoices.md) | GET |  |

### Issue

| Action | Method | Description |
| --- | --- | --- |
| [Create Issue](actions/create-issue.md) | POST | Creates a new issue in your Aspire account. |

### Item Allocation

| Action | Method | Description |
| --- | --- | --- |
| [Create Item Allocation](actions/create-item-allocation.md) | POST | Creates a new pay code in your Aspire account. |
| [List Item Allocations](actions/list-item-allocations.md) | GET |  |
| [Update Item Allocation](actions/update-item-allocation.md) | PUT |  |

### Job

| Action | Method | Description |
| --- | --- | --- |
| [List Job Statuses](actions/list-job-statuses.md) | GET | Retrieves job statuses from your Aspire account. |
| [List Jobs](actions/list-jobs.md) | GET | Retrieves jobs from your Aspire account. |

### Locality

| Action | Method | Description |
| --- | --- | --- |
| [Create Locality](actions/create-locality.md) | POST | Creates a new locality in your Aspire account. |
| [Update Locality](actions/update-locality.md) | PUT | Updates an existing locality in your Aspire account. |

### Locations

| Action | Method | Description |
| --- | --- | --- |
| [List Inventory Locations](actions/list-inventory-locations.md) | GET | Retrieves inventory locations from your Aspire account. |

### Opportunities

| Action | Method | Description |
| --- | --- | --- |
| [Create Estimate](actions/create-estimate.md) | POST | Retrieves takeoff groups from your Aspire account. |
| [Create Opportunity](actions/create-new-opportunity.md) | POST | Updates an existing pay code in your Aspire account. |
| [List Oportunity Service Items](actions/list-oportunity-service-items.md) | GET | Individual equipment, labor/subcontractors, or materials within the scope of a service on an estimate. |
| [List Opportunities](actions/list-opportunities.md) | GET |  |
| [List Opportunity Service Groups](actions/list-opportunity-service-groups.md) | GET |  |
| [List Opportunity Status](actions/list-opportunity-status.md) | GET | Retrieves opportunity statuses from your Aspire account. |

### Opportunity

| Action | Method | Description |
| --- | --- | --- |
| [List Opportunity Lost Reasons](actions/list-opportunity-lost-reasons.md) | GET | Retrieves opportunity lost reasons from your Aspire account. |
| [List Opportunity Service Kit Items](actions/list-opportunity-service-kit-items.md) | GET | Retrieves opportunity service kit items from your Aspire account. |
| [List Opportunity Services](actions/list-opportunity-services.md) | GET |  |

### Opportunity Lost Reason

| Action | Method | Description |
| --- | --- | --- |
| [Create Opportunity Lost Reason](actions/create-opportunity-lost-reason.md) | POST | Creates a new opportunity lost reason in your Aspire account. |
| [Update Opportunity Lost Reason](actions/update-opportunity-lost-reason.md) | PUT | Updates an existing opportunity lost reason in your Aspire account. |

### Opportunity Tag

| Action | Method | Description |
| --- | --- | --- |
| [Create Opportunity Tag](actions/create-opportunity-tag.md) | POST | Creates a new opportunity tag in your Aspire account. |
| [Delete Opportunity Tag](actions/delete-opportunity-tag.md) | DELETE | Deletes an existing opportunity tag from your Aspire account. |

### Pay Groups

| Action | Method | Description |
| --- | --- | --- |
| [Create Pay Codes](actions/create-pay-codes.md) | POST | Creates a new pay code in your Aspire account. |
| [Get Pay Codes](actions/get-pay-codes.md) | GET | Retrieves pay codes from your Aspire account. |
| [Update Pay Codes](actions/update-pay-codes.md) | PUT | Updates an existing pay code in your Aspire account. |

### Pay Schedule

| Action | Method | Description |
| --- | --- | --- |
| [Update Pay Schedule](actions/update-pay-schedule.md) | PUT | Updates an existing pay schedule in your Aspire account. |

### Payment Category

| Action | Method | Description |
| --- | --- | --- |
| [List Payment Categories](actions/list-payment-categories.md) | GET | Retrieves payment categories from your Aspire account. |

### Payment Terms

| Action | Method | Description |
| --- | --- | --- |
| [List Payment Terms](actions/list-payment-terms.md) | GET |  |

### Payments

| Action | Method | Description |
| --- | --- | --- |
| [Create Partial Payment](actions/create-partial-payment.md) | POST |  |
| [Create Partial Payment – Stripe to Aspire Sync](actions/create-partial-payment-stripe-to-aspire-sync.md) | POST |  |
| [List Payments](actions/list-payments.md) | GET |  |
| [List Payments – Stripe to Aspire Sync](actions/list-payments-stripe-to-aspire-sync.md) | GET |  |

### Payrolls

| Action | Method | Description |
| --- | --- | --- |
| [Create Pay Rate](actions/create-pay-rate.md) | POST | Creates a new pay code in your Aspire account. |
| [Create Pay Rate Override Pay Codes](actions/create-pay-rate-override-pay-codes.md) | POST | Creates a new pay rate override pay code in your Aspire account. |
| [Create Pay Schedule](actions/create-pay-schedule.md) | POST |  |
| [List Pay Rate Override Pay Codes](actions/list-pay-rate-override-pay-codes.md) | GET | Retrieves pay rate override pay codes from your Aspire account. |
| [List Pay Rates](actions/list-pay-rates.md) | GET |  |
| [Update Pay Rate](actions/update-pay-rate.md) | PUT |  |
| [Update Pay Rate Override Pay Codes](actions/update-pay-rate-override-pay-codes.md) | PUT | Updates an existing pay rate override pay code in your Aspire account. |

### Property

| Action | Method | Description |
| --- | --- | --- |
| [Create Property](actions/create-property.md) | POST |  |
| [Create Property Availability](actions/create-property-availability.md) | POST | Creates a new property availability in your Aspire account. |
| [Create Property Contact](actions/create-property-contact.md) | POST | Creates a new property contact in your Aspire account. |
| [List Properties](actions/list-properties.md) | GET | List physical locations where work is performed. Click Property for more information. |
| [List Property Availabilities](actions/list-property-availabilities.md) | GET | Retrieves property availability records from your Aspire account. |
| [List Property Contacts](actions/list-property-contacts.md) | GET |  |
| [List Property Status](actions/list-property-status.md) | GET | Retrieves property statuses from your Aspire account. |
| [List Property Types](actions/list-property-types.md) | GET |  |
| [Update Property](actions/update-property.md) | PUT | Updates a Property in Aspire |
| [Update Property Contacts](actions/update-property-contacts.md) | PUT |  |

### Propertycustomfields

| Action | Method | Description |
| --- | --- | --- |
| [List Property Custom Field Definitions](actions/list-property-custom-field-definitions.md) | GET | Retrieves property custom field definitions from your Aspire account. |
| [List Property Custom Fields](actions/list-property-custom-fields.md) | GET |  |

### Region

| Action | Method | Description |
| --- | --- | --- |
| [List Regions](actions/list-regions.md) | GET | Retrieves regions from your Aspire account. |

### Revenue Variance

| Action | Method | Description |
| --- | --- | --- |
| [List Revenue Variances](actions/list-revenue-variances.md) | GET | Retrieves revenue variances from your Aspire account. |

### Route

| Action | Method | Description |
| --- | --- | --- |
| [List Routes](actions/list-routes.md) | GET |  |

### Sales Type

| Action | Method | Description |
| --- | --- | --- |
| [List Localities](actions/list-localities.md) | GET | Retrieves localities from your Aspire account. |
| [List Sales Types](actions/list-sales-types.md) | GET | Retrieves sales types from your Aspire account. |

### Service

| Action | Method | Description |
| --- | --- | --- |
| [List Services](actions/list-services.md) | GET |  |

### Service Tax Override

| Action | Method | Description |
| --- | --- | --- |
| [Create Service Tax Override](actions/create-service-tax-override.md) | POST | Creates a new service tax override in your Aspire account. |
| [Update Service Tax Override](actions/update-service-tax-override.md) | PUT | Updates an existing service tax override in your Aspire account. |

### Service Type

| Action | Method | Description |
| --- | --- | --- |
| [List Service Type Integration Codes](actions/list-service-type-integration-codes.md) | GET | Retrieves service type integration codes from your Aspire account. |
| [List Service Types](actions/list-service-types.md) | GET | Retrieves service types from your Aspire account. |

### Tags

| Action | Method | Description |
| --- | --- | --- |
| [List Opportunity Tags](actions/list-opportunity-tags.md) | GET | Retrieves opportunity tags from your Aspire account. |
| [List Opportunity Tags Assignments](actions/list-opportunity-tags-assignments.md) | GET | Retrieves opportunity tags from your Aspire account. |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Create Task](actions/create-task.md) | POST | Creates a new task in your Aspire account. |

### Tax Entity

| Action | Method | Description |
| --- | --- | --- |
| [Create Tax Entity](actions/create-tax-entity.md) | POST | Creates a new tax entity in your Aspire account. |
| [Update Tax Entity](actions/update-tax-entity.md) | PUT | Updates an existing tax entity in your Aspire account. |

### Tax Jurisdiction

| Action | Method | Description |
| --- | --- | --- |
| [Create Tax Jurisdiction](actions/create-tax-jurisdiction.md) | POST | Creates a new tax jurisdiction in your Aspire account. |
| [Update Tax Jurisdiction](actions/update-tax-jurisdiction.md) | PUT | Updates an existing tax jurisdiction in your Aspire account. |

### Ticket

| Action | Method | Description |
| --- | --- | --- |
| [List Tags](actions/list-tags.md) | GET | Retrieves takeoff items from your Aspire account. |

### Tickets

| Action | Method | Description |
| --- | --- | --- |
| [List Prospect Ratings](actions/get-prospect-ratings.md) | GET |  |

### Unit Type

| Action | Method | Description |
| --- | --- | --- |
| [Create Unit Type](actions/create-unit-type.md) | POST | Creates a new unit type in your Aspire account. |
| [List Unit Types](actions/list-unit-types.md) | GET | Retrieves unit types from your Aspire account. |
| [Update Unit Type](actions/update-unit-type.md) | PUT | Updates an existing unit type in your Aspire account. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Create User](actions/create-user.md) | POST | Retrieves pay codes from your Aspire account. |

### Vendors

| Action | Method | Description |
| --- | --- | --- |
| [Create Vendor](actions/create-vendor.md) | POST |  |
| [List Vendors](actions/get-users.md) | GET |  |
| [Update Vendor](actions/update-vendor.md) | PUT |  |

### Work Ticket

| Action | Method | Description |
| --- | --- | --- |
| [Create As Needed Work Tickets](actions/create-work-ticket.md) | POST |  |
| [Create Work Ticket Time](actions/create-work-ticket-time.md) | POST | Creates a new work ticket time in your Aspire account. |
| [List Work Ticket Canceled Reasons](actions/list-work-ticket-canceled-reasons.md) | GET | Retrieves work ticket canceled reasons from your Aspire account. |
| [List Work Ticket Items](actions/list-work-ticket-items.md) | GET | Retrieves work ticket items from your Aspire account. |
| [List Work Ticket Revenues](actions/list-work-ticket-revenues.md) | GET | Total income generated within a work ticket. |
| [List Work Ticket Times](actions/list-work-ticket-times.md) | GET | Start and end time for a crew member during a visit for a work ticket. |
| [List Work Ticket Visit Notes](actions/list-work-ticket-visit-notes.md) | GET | Retrieves work ticket visit notes from your Aspire account. |
| [List Work Ticket Visits](actions/list-work-ticket-visits.md) | GET | Retrieves work ticket visits from your Aspire account. |
| [List Work Tickets](actions/list-work-tickets.md) | GET | Retrieves takeoff items from your Aspire account. |
| [Mark Work Ticket As Reviewed](actions/mark-work-ticket-as-reviewed.md) | PUT | Marks a work ticket as reviewed in your Aspire account. |

### Workers Comp

| Action | Method | Description |
| --- | --- | --- |
| [Create Workers Comp](actions/create-workers-comp.md) | POST | Creates a new workers comp record in your Aspire account. |
| [Update Workers Comp](actions/update-workers-comp.md) | PUT | Updates an existing workers comp record in your Aspire account. |

