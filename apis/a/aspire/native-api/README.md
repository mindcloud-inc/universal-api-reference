# Aspire: Native API Reference

A consolidated summary of Aspire's API configuration and 151 documented operations, with links to official documentation.

- **Official docs:** https://guide.youraspire.com/apidocs
- **API base URL:** `https://{environment}.youraspire.com/`

## Authentication

### Custom

### Credentials

- **Client ID:** `clientId` · required
- **Secret:** `secret` · required
- **Environment:** `environment` · required

Send these headers with each API request:

```http
Authorization: Bearer <custom.token>
```

[Official authentication documentation](https://guide.youraspire.com/apidocs/authentication-authorization-2)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

## Pagination

Use `$limit` in the query string to set the page size (default 25; maximum 1000). Use `$pageNumber` in the query string to choose the page; numbering starts at 1.

## Filtering

Send filters in the query string. Supported operators: `eq`, `gt`, `gte`, `lt`, `lte`, `ne`.

## Sorting

Set the sort field with `$orderby` in the query string. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Retry behavior

Wait 60000 ms before the first retry. Stop after 14 attempts. Multiply the delay by 3 after each failed attempt.

## Endpoints (151 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Approve Receipt](actions/approve-receipt.md) | `POST Receipts/Approve` | [docs](https://guide.youraspire.com/apidocs/receiptsapprove) |
| [Authenticate](actions/authenticate.md) | `POST Authorization` | [docs](https://guide.youraspire.com/apidocs/authorization-7) |
| [Create Catalog Item](actions/create-catalog-item.md) | `POST CatalogItems` | [docs](https://cloud-api.youraspire.com/swagger/index.html#/CatalogItems/CatalogItems_Create) |
| [Create Clock Time](actions/create-clock-time.md) | `POST ClockTimes` | [docs](https://guide.youraspire.com/apidocs/clocktimes-5) |
| [Create Company](actions/create-companies.md) | `POST Companies` | [docs](https://cloud-api.youraspire.com/swagger/index.html) |
| [Create Contact](actions/create-contact.md) | `POST Contacts` | [docs](https://guide.youraspire.com/apidocs/contacts-6) |
| [Create Contact Custom Field](actions/create-contact-custom-field.md) | `POST ContactCustomFields` | [docs](https://guide.youraspire.com/apidocs/propertycustomfields-7) |
| [Create Equipment Reading Log](actions/create-equipment-reading-log.md) | `POST EquipmentReadingLogs` | [docs](https://cloud-api.youraspire.com/swagger/index.html#/EquipmentReadingLogs/EquipmentReadingLogs_Create) |
| [Create Estimate](actions/create-estimate.md) | `POST Opportunities/EstimateImport` |  |
| [Create Issue](actions/create-issue.md) | `POST Issues` | [docs](https://guide.youraspire.com/apidocs/issues-4) |
| [Create Item Allocation](actions/create-item-allocation.md) | `POST ItemAllocations` | [docs](https://guide.youraspire.com/apidocs/itemallocations-3) |
| [Create Locality](actions/create-locality.md) | `POST Localities` | [docs](https://cloud-api.youraspire.com/swagger/index.html#/Localities/Localities_Create) |
| [Create Opportunity](actions/create-new-opportunity.md) | `POST Opportunities` | [docs](https://guide.youraspire.com/apidocs/opportunities-9) |
| [Create Opportunity Lost Reason](actions/create-opportunity-lost-reason.md) | `POST OpportunityLostReasons` | [docs](https://cloud-api.youraspire.com/swagger/index.html#/OpportunityLostReasons/OpportunityLostReasons_Create) |
| [Create Opportunity Tag](actions/create-opportunity-tag.md) | `POST OpportunityTags` | [docs](https://cloud-api.youraspire.com/swagger/index.html#/OpportunityTags/OpportunityTags_Create) |
| [Create Partial Payment](actions/create-partial-payment.md) | `POST PartialPayments` | [docs](https://guide.youraspire.com/v1-api/apidocs/en/partialpayments-4) |
| [Create Pay Codes](actions/create-pay-codes.md) | `POST PayCodes` | [docs](https://guide.youraspire.com/apidocs/paycodes-10) |
| [Create Pay Rate](actions/create-pay-rate.md) | `POST PayRates` | [docs](https://guide.youraspire.com/apidocs/payrates-6) |
| [Create Pay Rate Override Pay Codes](actions/create-pay-rate-override-pay-codes.md) | `POST PayRateOverridePayCodes` | [docs](https://guide.youraspire.com/apidocs/payrates-5) |
| [Create Pay Schedule](actions/create-pay-schedule.md) | `POST PaySchedules` | [docs](https://guide.youraspire.com/apidocs/payschedules-3) |
| [Create Property](actions/create-property.md) | `POST Properties` | [docs](https://cloud-api.youraspire.com/swagger/index.html) |
| [Create Property Availability](actions/create-property-availability.md) | `POST PropertyAvailabilities` | [docs](https://cloud-api.youraspire.com/swagger/index.html#/PropertyAvailabilities/PropertyAvailabilities_Create) |
| [Create Property Contact](actions/create-property-contact.md) | `POST PropertyContacts` | [docs](https://cloud-api.youraspire.com/swagger/index.html#/PropertyContacts/PropertyContacts_Create) |
| [Create Receipt](actions/create-receipt.md) | `POST Receipts` | [docs](https://guide.youraspire.com/apidocs/receipts-9) |
| [Create Service Tax Override](actions/create-service-tax-override.md) | `POST ServiceTaxOverrides` | [docs](https://cloud-api.youraspire.com/swagger/index.html#/ServiceTaxOverrides/ServiceTaxOverrides_Post) |
| [Create Task](actions/create-task.md) | `POST Tasks` | [docs](https://guide.youraspire.com/apidocs/tasks-6) |
| [Create Tax Entity](actions/create-tax-entity.md) | `POST TaxEntities` | [docs](https://cloud-api.youraspire.com/swagger/index.html#/TaxEntities/TaxEntities_Post) |
| [Create Tax Jurisdiction](actions/create-tax-jurisdiction.md) | `POST TaxJurisdictions` | [docs](https://cloud-api.youraspire.com/swagger/index.html#/TaxJurisdictions/TaxJurisdictions_Post) |
| [Create Unit Type](actions/create-unit-type.md) | `POST UnitTypes` | [docs](https://cloud-api.youraspire.com/swagger/index.html#/UnitTypes/UnitTypes_Create) |
| [Create User](actions/create-user.md) | `POST Users` | [docs](https://guide.youraspire.com/apidocs/users-8) |
| [Create Vendor](actions/create-vendor.md) | `POST Vendors` | [docs](https://guide.youraspire.com/apidocs/vendors-3) |
| [Create As Needed Work Tickets](actions/create-work-ticket.md) | `POST WorkTickets/CreateAsNeededWorkTickets` | [docs](https://guide.youraspire.com/apidocs/workticketscreateasneededworktickets-1) |
| [Create Work Ticket Time](actions/create-work-ticket-time.md) | `POST WorkTicketTimes` | [docs](https://cloud-api.youraspire.com/swagger/index.html#/WorkTicketTimes/WorkTicketTimes_Create) |
| [Create Workers Comp](actions/create-workers-comp.md) | `POST WorkersComps` | [docs](https://cloud-api.youraspire.com/swagger/index.html#/WorkersComps/WorkersComps_Create) |
| [Delete Opportunity Tag](actions/delete-opportunity-tag.md) | `DELETE OpportunityTags/:id` | [docs](https://cloud-api.youraspire.com/swagger/index.html#/OpportunityTags/OpportunityTags_Delete) |
| [Get API Version](actions/get-api-version.md) | `GET Version/GetApiVersion` | [docs](https://cloud-api.youraspire.com/swagger/index.html#/Version/Version_GetApiVersion) |
| [Get Attachment File Data](actions/get-attachment-file-data.md) | `GET Attachments/AttachmentFileData` | [docs](https://guide.youraspire.com/apidocs/attachmentsattachmentfiledata-1) |
| [Get Workers Comps](actions/get-contact-types.md) | `GET WorkersComps` | [docs](https://guide.youraspire.com/apidocs/contacttypes-3) |
| [List Invoice Revenues](actions/get-invoice-revenue.md) | `GET invoicerevenues` | [docs](https://guide.youraspire.com/apidocs/invoicerevenues-3) |
| [Get Pay Codes](actions/get-pay-codes.md) | `GET PayCodes` | [docs](https://guide.youraspire.com/apidocs/paycodes-9) |
| [List Prospect Ratings](actions/get-prospect-ratings.md) | `GET ProspectRatings` | [docs](https://guide.youraspire.com/apidocs/prospectratings-3) |
| [List Vendors](actions/get-users.md) | `GET Vendors` | [docs](https://guide.youraspire.com/apidocs/vendors-6) |
| [List Activities](actions/list-activities.md) | `GET Activities` | [docs](https://guide.youraspire.com/apidocs/) |
| [List Activity Categories](actions/list-activity-categories.md) | `GET ActivityCategories` | [docs](https://guide.youraspire.com/apidocs/activitycategories-6) |
| [List Activity Comment Histories](actions/list-activity-comment-histories.md) | `GET ActivityCommentHistories` | [docs](https://cloud-api.youraspire.com/swagger/index.html#/ActivityCommentHistories/ActivityCommentHistories_Get) |
| [List Activity Contacts](actions/list-activity-contacts.md) | `GET ActivityContacts` | [docs](https://cloud-api.youraspire.com/swagger/index.html#/ActivityContacts/ActivityContacts_Get) |
| [List Addresses](actions/list-addresses.md) | `GET Addresses` | [docs](https://cloud-api.youraspire.com/swagger/v1/swagger.json) |
| [List Attachment Types](actions/list-attachment-types.md) | `GET AttachmentTypes` | [docs](https://guide.youraspire.com/apidocs/attachmenttypes-3) |
| [List Attachments](actions/list-attachments.md) | `GET Attachments` | [docs](https://guide.youraspire.com/apidocs/attachments-5) |
| [List Bank Deposits](actions/list-bank-deposits.md) | `GET BankDeposits` | [docs](https://guide.youraspire.com/apidocs/bankdeposits-6) |
| [List Branches](actions/list-branches.md) | `GET Branches` | [docs](https://guide.youraspire.com/apidocs/branches-7) |
| [List Catalog Item Categories](actions/list-catalog-item-categories.md) | `GET /CatalogItemCategories` | [docs](https://guide.youraspire.com/apidocs/catalogitemcategories-3) |
| [List Catalog Items](actions/list-catalog-items.md) | `GET CatalogItems` | [docs](https://guide.youraspire.com/apidocs/catalogitems-5) |
| [List Certification Types](actions/list-certification-types.md) | `GET CertificationTypes` | [docs](https://cloud-api.youraspire.com/swagger/index.html#/CertificationTypes/CertificationTypes_Get) |
| [List Certifications](actions/list-certifications.md) | `GET Certifications` | [docs](https://cloud-api.youraspire.com/swagger/index.html#/Certifications/Certifications_Get) |
| [List Clock Times](actions/list-clock-times.md) | `GET ClockTimes` | [docs](https://guide.youraspire.com/apidocs/clocktimes-2) |
| [List Companies](actions/list-companies.md) | `GET Companies` | [docs](https://guide.youraspire.com/apidocs/companies-6) |
| [List Contact Custom Field Definitions](actions/list-contact-custom-field-definitions.md) | `GET ContactCustomFieldDefinitions` | [docs](https://guide.youraspire.com/apidocs/propertycustomfields-7) |
| [List Contact Custom Fields](actions/list-contact-custom-fields.md) | `GET ContactCustomFields` | [docs](https://guide.youraspire.com/apidocs/propertycustomfields-7) |
| [List Contact Types](actions/list-contact-types.md) | `GET ContactTypes` | [docs](https://guide.youraspire.com/apidocs/contacttypes-3) |
| [List Contacts](actions/list-contacts.md) | `GET Contacts` | [docs](https://guide.youraspire.com/apidocs/contacts-12) |
| [List Division Integration Codes](actions/list-division-integration-codes.md) | `GET DivisionIntegrationCodes` | [docs](https://cloud-api.youraspire.com/swagger/index.html#/DivisionIntegrationCodes/DivisionIntegrationCodes_Get) |
| [List Divisions](actions/list-divisions.md) | `GET Divisions` | [docs](https://guide.youraspire.com/apidocs/divisions-7) |
| [List Employee Incident Types](actions/list-employee-incident-types.md) | `GET EmployeeIncidentTypes` | [docs](https://cloud-api.youraspire.com/swagger/index.html#/EmployeeIncidentTypes/EmployeeIncidentTypes_Get) |
| [List Employee Incidents](actions/list-employee-incidents.md) | `GET EmployeeIncidents` | [docs](https://guide.youraspire.com/apidocs/contacts-3) |
| [List Equipment Classes](actions/list-equipment-classes.md) | `GET EquipmentClasses` | [docs](https://cloud-api.youraspire.com/swagger/index.html#/EquipmentClasses/EquipmentClasses_Get) |
| [List Equipment Disposal Reasons](actions/list-equipment-disposal-reasons.md) | `GET EquipmentDisposalReasons` | [docs](https://cloud-api.youraspire.com/swagger/index.html#/EquipmentDisposalReasons/EquipmentDisposalReasons_Get) |
| [List Equipment Manufacturers](actions/list-equipment-manufacturers.md) | `GET EquipmentManufacturers` | [docs](https://cloud-api.youraspire.com/swagger/index.html#/EquipmentManufacturers/EquipmentManufacturers_Get) |
| [List Equipment Model Service Schedules](actions/list-equipment-model-service-schedules.md) | `GET EquipmentModelServiceSchedules` | [docs](https://cloud-api.youraspire.com/swagger/index.html#/EquipmentModelServiceSchedules/EquipmentModelServiceSchedules_Get) |
| [List Equipment Models](actions/list-equipment-models.md) | `GET EquipmentModels` | [docs](https://cloud-api.youraspire.com/swagger/index.html#/EquipmentModels/EquipmentModels_Get) |
| [List Equipment Reading Logs](actions/list-equipment-reading-logs.md) | `GET EquipmentReadingLogs` | [docs](https://cloud-api.youraspire.com/swagger/index.html#/EquipmentReadingLogs/EquipmentReadingLogs_Get) |
| [List Equipment Requested Services](actions/list-equipment-requested-services.md) | `GET EquipmentRequestedServices` | [docs](https://cloud-api.youraspire.com/swagger/index.html#/EquipmentRequestedServices/EquipmentRequestedServices_Get) |
| [List Equipment Service Logs](actions/list-equipment-service-logs.md) | `GET EquipmentServiceLogs` | [docs](https://cloud-api.youraspire.com/swagger/index.html#/EquipmentServiceLogs/EquipmentServiceLogs_Get) |
| [List Equipment Service Tags](actions/list-equipment-service-tags.md) | `GET EquipmentServiceTags` | [docs](https://cloud-api.youraspire.com/swagger/index.html#/EquipmentServiceTags/EquipmentServiceTags_Get) |
| [List Equipment Sizes](actions/list-equipment-sizes.md) | `GET EquipmentSizes` | [docs](https://cloud-api.youraspire.com/swagger/index.html#/EquipmentSizes/EquipmentSizes_Get) |
| [List Equipments](actions/list-equipments.md) | `GET Equipments` | [docs](https://guide.youraspire.com/apidocs/equipments-6) |
| [List Inventory Locations](actions/list-inventory-locations.md) | `GET InventoryLocations` | [docs](https://guide.youraspire.com/apidocs/inventorylocations-6) |
| [List Invoice Batches](actions/list-invoice-batches.md) | `GET InvoiceBatches` | [docs](https://cloud-api.youraspire.com/swagger/index.html#/) |
| [List Invoice Taxes](actions/list-invoice-taxes.md) | `GET InvoiceTaxes` | [docs](https://cloud-api.youraspire.com/swagger/index.html#/InvoiceTaxes/InvoiceTaxes_Get) |
| [List Invoices](actions/list-invoices.md) | `GET invoices` | [docs](https://guide.youraspire.com/apidocs/invoices-4) |
| [List Item Allocations](actions/list-item-allocations.md) | `GET ItemAllocations` | [docs](https://guide.youraspire.com/apidocs/itemallocations-2) |
| [List Job Statuses](actions/list-job-statuses.md) | `GET JobStatuses` | [docs](https://cloud-api.youraspire.com/swagger/index.html#/JobStatuses/JobStatuses_Get) |
| [List Jobs](actions/list-jobs.md) | `GET Jobs` | [docs](https://cloud-api.youraspire.com/swagger/index.html#/Jobs/Jobs_Get) |
| [List Localities](actions/list-localities.md) | `GET Localities` | [docs](https://guide.youraspire.com/apidocs) |
| [List Oportunity Service Items](actions/list-oportunity-service-items.md) | `GET OpportunityServiceItems` | [docs](https://guide.youraspire.com/apidocs/opportunityserviceitems-3) |
| [List Opportunities](actions/list-opportunities.md) | `GET Opportunities` | [docs](https://guide.youraspire.com/apidocs/opportunities-2) |
| [List Opportunity Lost Reasons](actions/list-opportunity-lost-reasons.md) | `GET OpportunityLostReasons` | [docs](https://cloud-api.youraspire.com/swagger/index.html#/OpportunityLostReasons/OpportunityLostReasons_Get) |
| [List Opportunity Service Groups](actions/list-opportunity-service-groups.md) | `GET OpportunityServiceGroups` | [docs](https://guide.youraspire.com/apidocs/opportunityservicegroups-5) |
| [List Opportunity Service Kit Items](actions/list-opportunity-service-kit-items.md) | `GET OpportunityServiceKitItems` | [docs](https://cloud-api.youraspire.com/swagger/index.html#/OpportunityServiceKitItems/OpportunityServiceKitItems_Get) |
| [List Opportunity Services](actions/list-opportunity-services.md) | `GET OpportunityServices` | [docs](https://guide.youraspire.com/apidocs/) |
| [List Opportunity Status](actions/list-opportunity-status.md) | `GET OpportunityStatuses` | [docs](https://guide.youraspire.com/apidocs/opportunity-status) |
| [List Opportunity Tags](actions/list-opportunity-tags.md) | `GET OpportunityTags` | [docs](https://cloud-api.youraspire.com/swagger/index.html) |
| [List Opportunity Tags Assignments](actions/list-opportunity-tags-assignments.md) | `GET OpportunityTags` | [docs](https://cloud-api.youraspire.com/swagger/index.html) |
| [List Pay Rate Override Pay Codes](actions/list-pay-rate-override-pay-codes.md) | `GET PayRateOverridePayCodes` | [docs](https://guide.youraspire.com/apidocs/payrates-5) |
| [List Pay Rates](actions/list-pay-rates.md) | `GET PayRates` | [docs](https://guide.youraspire.com/apidocs/payrates-5) |
| [List Pay Schedules](actions/list-pay-schedules.md) | `GET PaySchedules` | [docs](https://guide.youraspire.com/apidocs/pay-schedules-1) |
| [List Payment Categories](actions/list-payment-categories.md) | `GET PaymentCategories` | [docs](https://cloud-api.youraspire.com/swagger/index.html#/PaymentCategories/PaymentCategories_Get) |
| [List Payment Terms](actions/list-payment-terms.md) | `GET PaymentTerms` | [docs](https://guide.youraspire.com/apidocs/paymentterms-3) |
| [List Payments](actions/list-payments.md) | `GET Payments` | [docs](https://guide.youraspire.com/apidocs/payments-4) |
| [List Properties](actions/list-properties.md) | `GET Properties` | [docs](https://guide.youraspire.com/apidocs/properties-2) |
| [List Property Availabilities](actions/list-property-availabilities.md) | `GET PropertyAvailabilities` | [docs](https://cloud-api.youraspire.com/swagger/index.html#/PropertyAvailabilities/PropertyAvailabilities_Get) |
| [List Property Contacts](actions/list-property-contacts.md) | `GET PropertyContacts` | [docs](https://guide.youraspire.com/apidocs/propertycontacts-5) |
| [List Property Custom Field Definitions](actions/list-property-custom-field-definitions.md) | `GET PropertyCustomFieldDefinitions` | [docs](https://cloud-api.youraspire.com/swagger/index.html#/PropertyCustomFieldDefinitions/PropertyCustomFieldDefinitions_Get) |
| [List Property Custom Fields](actions/list-property-custom-fields.md) | `GET PropertyCustomFields` | [docs](https://guide.youraspire.com/apidocs/propertycustomfields-7) |
| [List Property Status](actions/list-property-status.md) | `GET PropertyStatuses` | [docs](https://guide.youraspire.com/apidocs/propertytypes-3) |
| [List Property Types](actions/list-property-types.md) | `GET PropertyTypes` | [docs](https://guide.youraspire.com/apidocs/propertytypes-3) |
| [List Receipts](actions/list-receipts.md) | `GET Receipts` | [docs](https://guide.youraspire.com/apidocs/receipts-5) |
| [List Regions](actions/list-regions.md) | `GET Regions` | [docs](https://cloud-api.youraspire.com/swagger/index.html#/Regions/Regions_Get) |
| [List Revenue Variances](actions/list-revenue-variances.md) | `GET RevenueVariances` | [docs](https://cloud-api.youraspire.com/swagger/index.html#/RevenueVariances/RevenueVariances_Get) |
| [List Roles](actions/list-roles.md) | `GET Roles` | [docs](https://guide.youraspire.com/apidocs/roles-3) |
| [List Routes](actions/list-routes.md) | `GET Routes` | [docs](https://guide.youraspire.com/apidocs/routes-4) |
| [List Sales Types](actions/list-sales-types.md) | `GET SalesTypes` | [docs](https://guide.youraspire.com/apidocs) |
| [List Service Type Integration Codes](actions/list-service-type-integration-codes.md) | `GET ServiceTypeIntegrationCodes` | [docs](https://cloud-api.youraspire.com/swagger/index.html#/ServiceTypeIntegrationCodes/ServiceTypeIntegrationCodes_Get) |
| [List Service Types](actions/list-service-types.md) | `GET ServiceTypes` | [docs](https://cloud-api.youraspire.com/swagger/index.html#/ServiceTypes/ServiceTypes_Get) |
| [List Services](actions/list-services.md) | `GET Services` | [docs](https://guide.youraspire.com/apidocs) |
| [List Tags](actions/list-tags.md) | `GET Tags` | [docs](https://cloud-api.youraspire.com/swagger/index.html) |
| [List Tax Jurisdictions](actions/list-tax-jurisdictions.md) | `GET TaxJurisdictions` | [docs](https://guide.youraspire.com/apidocs/divisions-7) |
| [List Unit Types](actions/list-unit-types.md) | `GET UnitTypes` | [docs](https://cloud-api.youraspire.com/swagger/index.html#/UnitTypes/UnitTypes_Get) |
| [List Users](actions/list-users.md) | `GET Users` | [docs](https://guide.youraspire.com/apidocs/users-11) |
| [List Work Ticket Canceled Reasons](actions/list-work-ticket-canceled-reasons.md) | `GET WorkTicketCanceledReasons` | [docs](https://cloud-api.youraspire.com/swagger/index.html#/WorkTicketCanceledReasons/WorkTicketCanceledReasons_Get) |
| [List Work Ticket Items](actions/list-work-ticket-items.md) | `GET WorkTicketItems` | [docs](https://guide.youraspire.com/apidocs/workticketitems-3) |
| [List Work Ticket Revenues](actions/list-work-ticket-revenues.md) | `GET WorkTicketRevenues` | [docs](https://guide.youraspire.com/apidocs/workticketrevenues-3) |
| [List Work Ticket Times](actions/list-work-ticket-times.md) | `GET WorkTicketTimes` | [docs](https://guide.youraspire.com/apidocs/worktickettimes-4) |
| [List Work Ticket Visit Notes](actions/list-work-ticket-visit-notes.md) | `GET WorkTicketVisitNotes` | [docs](https://cloud-api.youraspire.com/swagger/index.html#/WorkTicketVisitNotes/WorkTicketVisitNotes_Get) |
| [List Work Ticket Visits](actions/list-work-ticket-visits.md) | `GET WorkTicketVisits` | [docs](https://cloud-api.youraspire.com/swagger/index.html#/WorkTicketVisits/WorkTicketVisits_Get) |
| [List Work Tickets](actions/list-work-tickets.md) | `GET WorkTickets` | [docs](https://guide.youraspire.com/apidocs/worktickets-3) |
| [Mark Work Ticket As Reviewed](actions/mark-work-ticket-as-reviewed.md) | `POST WorkTicketStatus/MarkWorkTicketAsReviewed` | [docs](https://cloud-api.youraspire.com/swagger/index.html#/WorkTicketStatus/WorkTicketStatus_MarkWorkTicketAsReviewed) |
| [Post Attachment](actions/post-attachment.md) | `POST /Attachments` | [docs](https://guide.youraspire.com/apidocs/attachments-2) |
| [Receive Receipt](actions/receive-receipt.md) | `POST Receipts/Receive` | [docs](https://guide.youraspire.com/apidocs/receiptsreceive) |
| [Refresh Authorization Token](actions/refresh-authorization-token.md) | `POST Authorization/RefreshToken` | [docs](https://cloud-api.youraspire.com/swagger/index.html#/Authorization/Authorization_RefreshToken) |
| [Update Catalog Item](actions/update-catalog-item.md) | `PUT CatalogItems` | [docs](https://cloud-api.youraspire.com/swagger/index.html#/CatalogItems/CatalogItems_Update) |
| [Update Company](actions/update-company.md) | `PUT Companies` | [docs](https://cloud-api.youraspire.com/swagger/index.html) |
| [Update Contact](actions/update-contact.md) | `PUT Contacts` | [docs](https://guide.youraspire.com/apidocs/contacts-2) |
| [Update Contact Custom Field](actions/update-contact-custom-field.md) | `PUT ContactCustomFields` | [docs](https://guide.youraspire.com/apidocs/propertycustomfields-7) |
| [Update Equipment Reading Log](actions/update-equipment-reading-log.md) | `PUT EquipmentReadingLogs` | [docs](https://cloud-api.youraspire.com/swagger/index.html#/EquipmentReadingLogs/EquipmentReadingLogs_Update) |
| [Update Item Allocation](actions/update-item-allocation.md) | `PUT ItemAllocations` | [docs](https://guide.youraspire.com/apidocs/itemallocations-12) |
| [Update Locality](actions/update-locality.md) | `PUT Localities` | [docs](https://cloud-api.youraspire.com/swagger/index.html#/Localities/Localities_Update) |
| [Update Opportunity Lost Reason](actions/update-opportunity-lost-reason.md) | `PUT OpportunityLostReasons` | [docs](https://cloud-api.youraspire.com/swagger/index.html#/OpportunityLostReasons/OpportunityLostReasons_Update) |
| [Update Pay Codes](actions/update-pay-codes.md) | `PUT PayCodes` | [docs](https://guide.youraspire.com/apidocs/paycodes-11) |
| [Update Pay Rate](actions/update-pay-rate.md) | `PUT PayRates` | [docs](https://guide.youraspire.com/apidocs/payrates-7) |
| [Update Pay Rate Override Pay Codes](actions/update-pay-rate-override-pay-codes.md) | `PUT PayRateOverridePayCodes` | [docs](https://guide.youraspire.com/apidocs/payrates-5) |
| [Update Pay Schedule](actions/update-pay-schedule.md) | `PUT PaySchedules` | [docs](https://cloud-api.youraspire.com/swagger/index.html#/PaySchedules/PaySchedules_Update) |
| [Update Property](actions/update-property.md) | `PUT Properties` | [docs](https://guide.youraspire.com/apidocs/properties-8) |
| [Update Property Contacts](actions/update-property-contacts.md) | `PUT PropertyContacts` | [docs](https://guide.youraspire.com/apidocs/propertycontacts-7) |
| [Update Service Tax Override](actions/update-service-tax-override.md) | `PUT ServiceTaxOverrides` | [docs](https://cloud-api.youraspire.com/swagger/index.html#/ServiceTaxOverrides/ServiceTaxOverrides_Put) |
| [Update Tax Entity](actions/update-tax-entity.md) | `PUT TaxEntities` | [docs](https://cloud-api.youraspire.com/swagger/index.html#/TaxEntities/TaxEntities_Update) |
| [Update Tax Jurisdiction](actions/update-tax-jurisdiction.md) | `PUT TaxJurisdictions` | [docs](https://cloud-api.youraspire.com/swagger/index.html#/TaxJurisdictions/TaxJurisdictions_Update) |
| [Update Unit Type](actions/update-unit-type.md) | `PUT UnitTypes` | [docs](https://cloud-api.youraspire.com/swagger/index.html#/UnitTypes/UnitTypes_Update) |
| [Update User](actions/update-user.md) | `PUT Users` | [docs](https://guide.youraspire.com/apidocs/users-7) |
| [Update Vendor](actions/update-vendor.md) | `PUT Vendors` | [docs](https://guide.youraspire.com/apidocs/vendors-12) |
| [Update Workers Comp](actions/update-workers-comp.md) | `PUT WorkersComps` | [docs](https://cloud-api.youraspire.com/swagger/index.html#/WorkersComps/WorkersComps_Update) |
