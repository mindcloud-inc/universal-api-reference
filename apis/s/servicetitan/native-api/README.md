# ServiceTitan: Native API Reference

A consolidated summary of ServiceTitan's API configuration and 102 documented operations, with links to official documentation.

- **Official docs:** https://developer.servicetitan.io/api-details/#api=tenant-crm-v2
- **API base URL:** `https://{baseUrl}/`

## Authentication

### OAuth 2.0 client credentials

ServiceTitan uses the OAuth 2.0 client-credentials flow. Exchange the client ID and client secret for an access token, then send the resulting authorization value together with the application key. The tenant ID is part of each resource path, and credentials are environment-specific.

### Credentials

- **Client ID:** `clientId` · required
- **Client Secret:** `clientScrt` · required
- **App Key:** `appKey` · required
- **Tenant:** `tenant` · required
- **Development Environment:** `developmentEnvironment` · optional · Use this to switch to the dev environment for testing

Send these headers with each API request:

```http
ST-App-Key: <appKey>
Authorization: <custom.accessToken>
```

[Official authentication documentation](https://developer.servicetitan.io/docs/getting-started/first-api-call)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

## Pagination

Use `pageSize` in the query string to set the page size (default 50; accepted range 1–1000). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (102 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Customer Tag](actions/add-customer-tag.md) | `POST crm/v2/tenant/{{credentials.tenant}}/customers/:customerId/tags/:tagTypeId` |  |
| [Create Booking](actions/create-booking.md) | `POST crm/v2/tenant/{{credentials.tenant}}/booking-provider/:bookingProviderId/bookings` | [docs](https://developer.servicetitan.io/api-details/#api=tenant-crm-v2&operation=Bookings_Create) |
| [Create Customer](actions/create-customer.md) | `POST crm/v2/tenant/{{credentials.tenant}}/customers` |  |
| [Create Customer Contact](actions/create-customer-contact.md) | `POST crm/v2/tenant/{{credentials.tenant}}/customers/:id/contacts` | [docs](https://developer.servicetitan.io/api-details/#api=tenant-crm-v2&operation=Customers_CreateContact) |
| [Create Customer Membership](actions/create-customer-membership.md) | `POST memberships/v2/tenant/{{credentials.tenant}}/memberships/sale` | [docs](https://developer.servicetitan.io/api-details/#api=tenant-memberships-v2&operation=CustomerMemberships_Create) |
| [Create GL Account](actions/create-gl-account.md) | `POST accounting/v2/tenant/{{credentials.tenant}}/gl-accounts` |  |
| [Create Job](actions/create-job.md) | `POST jpm/v2/tenant/{{credentials.tenant}}/jobs` |  |
| [Create Job Note](actions/create-job-note.md) | `POST jpm/v2/tenant/{{credentials.tenant}}/jobs/:id/notes` | [docs](https://developer.servicetitan.io/api-details/#api=tenant-jpm-v2&operation=Projects_CreateNote) |
| [Create Location](actions/create-location.md) | `POST crm/v2/tenant/{{credentials.tenant}}/locations` |  |
| [Create Payment](actions/create-payment.md) | `POST accounting/v2/tenant/{{credentials.tenant}}/payments` |  |
| [Create Project](actions/create-project.md) | `POST jpm/v2/tenant/{{credentials.tenant}}/projects` | [docs](https://developer.servicetitan.io/apis/) |
| [Create Project Note](actions/create-project-note.md) | `POST jpm/v2/tenant/{{credentials.tenant}}/projects/:id/notes` | [docs](https://developer.servicetitan.io/api-details/#api=tenant-jpm-v2&operation=Projects_CreateNote) |
| [Create Task](actions/create-task.md) | `POST taskmanagement/v2/tenant/{{credentials.tenant}}/tasks` | [docs](https://developer.servicetitan.io/api-details/#api=tenant-task-management-v2&operation=Tasks_Create) |
| [Get Task Management Data](actions/create-task-management-data.md) | `GET taskmanagement/v2/tenant/{{credentials.tenant}}/data` | [docs](https://developer.servicetitan.io/api-details/#api=tenant-task-management-v2&operation=Tasks_Create) |
| [Export Adjustments](actions/export-adjustments.md) | `GET inventory/v2/tenant/{{credentials.tenant}}/export/adjustments?:from&:includeRecentChanges` |  |
| [Export Job Notes](actions/export-job-notes.md) | `GET jpm/v2/tenant/{{credentials.tenant}}/export/job-notes` | [docs](https://developer.servicetitan.io/api-details/#api=tenant-jpm-v2&operation=Export_JobNotes) |
| [Export Project Notes](actions/export-project-notes.md) | `GET jpm/v2/tenant/{{credentials.tenant}}/export/project-notes` | [docs](https://developer.servicetitan.io/api-details/#api=tenant-jpm-v2&operation=Export_JobNotes) |
| [Export Purchase Orders](actions/export-purchase-orders.md) | `GET inventory/v2/tenant/{{credentials.tenant}}/export/purchase-orders?:from&:includeRecentChanges` |  |
| [Export Returns](actions/export-returns.md) | `GET inventory/v2/tenant/{{credentials.tenant}}/export/returns?:from&:includeRecentChanges` |  |
| [Export Transfers](actions/export-transfers.md) | `GET inventory/v2/tenant/{{credentials.tenant}}/export/transfers?:from&:includeRecentChanges` |  |
| [Get Access Token](actions/get-access-token.md) | `POST https://{{credentials.authUrl}}/connect/token` |  |
| [Get Appointment Assignments](actions/get-appointment-assignments.md) | `GET dispatch/v2/tenant/{{credentials.tenant}}/appointment-assignments` |  |
| [Get Appointment by Id](actions/get-appointment-by-id.md) | `GET https://api.servicetitan.io/jpm/v2/tenant/{{credentials.tenant}}/appointments/:id` |  |
| [Get Appointments](actions/get-appointments.md) | `GET https://api.servicetitan.io/jpm/v2/tenant/{{credentials.tenant}}/appointments/` | [docs](https://developer.servicetitan.io/api-details/#api=tenant-jpm-v2&operation=Appointments_GetList) |
| [Get Booking Providers](actions/get-booking-providers.md) | `GET crm/v2/tenant/{{credentials.tenant}}/booking-provider-tags` | [docs](https://developer.servicetitan.io/api-details/#api=tenant-crm-v2&operation=BookingProviderTags_GetList) |
| [Get Bookings](actions/get-bookings.md) | `GET crm/v2/tenant/{{credentials.tenant}}/bookings` | [docs](https://developer.servicetitan.io/api-details/#api=tenant-crm-v2&operation=Bookings_Create) |
| [Get Business Units](actions/get-business-units.md) | `GET settings/v2/tenant/{{credentials.tenant}}/business-units` | [docs](https://developer.servicetitan.io/api-details/#api=tenant-settings-v2&operation=BusinessUnits_GetList) |
| [Get Campaigns](actions/get-campaigns.md) | `GET https://api.servicetitan.io/marketing/v2/tenant/{{credentials.tenant}}/campaigns` |  |
| [Get Customer By Id](actions/get-customer-by-id.md) | `GET crm/v2/tenant/{{credentials.tenant}}/customers/:id` |  |
| [Get Customers](actions/get-customers.md) | `GET crm/v2/tenant/{{credentials.tenant}}/customers` |  |
| [Get Discount and Fees](actions/get-discount-and-fees.md) | `GET pricebook/v2/tenant/{{credentials.tenant}}/discounts-and-fees` | [docs](https://developer.servicetitan.io/api-details/#api=tenant-pricebook-v2&operation=DiscountAndFees_GetList) |
| [Get Employees](actions/get-employees.md) | `GET settings/v2/tenant/{{credentials.tenant}}/employees` | [docs](https://developer.servicetitan.io/api-details/#api=tenant-settings-v2&operation=Employees_GetList) |
| [Get Equipment by Id](actions/get-equipment-by-id.md) | `GET pricebook/v2/tenant/{{credentials.tenant}}/equipment/:id` |  |
| [Get Equipments](actions/get-equipments.md) | `GET pricebook/v2/tenant/{{credentials.tenant}}/equipment` | [docs](https://developer.servicetitan.io/api-details/#api=tenant-pricebook-v2&operation=Equipment_GetList) |
| [Get Forms](actions/get-forms.md) | `GET forms/v2/tenant/{{credentials.tenant}}/forms?:from&:includeRecentChanges` |  |
| [Get Forms Submissions](actions/get-forms-submissions.md) | `GET forms/v2/tenant/{{credentials.tenant}}/submissions` |  |
| [Get GL Account Types](actions/get-gl-account-types.md) | `GET accounting/v2/tenant/{{credentials.tenant}}/gl-accounts/types` |  |
| [Get GL Accounts](actions/get-gl-accounts.md) | `GET accounting/v2/tenant/{{credentials.tenant}}/gl-accounts` |  |
| [Get Invoices](actions/get-invoices.md) | `GET accounting/v2/tenant/{{credentials.tenant}}/invoices` | [docs](https://developer.servicetitan.io/api-details/#api=tenant-accounting-v2&operation=Invoices_GetList) |
| [Get Invoices By Job Id](actions/get-invoices-by-job-id.md) | `GET accounting/v2/tenant/{{credentials.tenant}}/invoices` | [docs](https://developer.servicetitan.io/api-details/#api=tenant-accounting-v2&operation=Invoices_GetList) |
| [Get Item Receipts](actions/get-item-receipts.md) | `GET inventory/v2/tenant/{{credentials.tenant}}/receipts` |  |
| [Get Job Notes](actions/get-job-notes.md) | `GET jpm/v2/tenant/{{credentials.tenant}}/jobs/:jobId/notes` |  |
| [Get Job Types](actions/get-job-types.md) | `GET https://api.servicetitan.io/jpm/v2/tenant/{{credentials.tenant}}/job-types` |  |
| [Get Lead Notes](actions/get-lead-notes.md) | `GET crm/v2/tenant/{{credentials.tenant}}/leads/:leadId/notes` | [docs](https://developer.servicetitan.io/api-details/#api=tenant-crm-v2&operation=Leads_GetNotes) |
| [Get Location By Id](actions/get-location-by-id.md) | `GET crm/v2/tenant/{{credentials.tenant}}/locations/:id` |  |
| [Get Locations](actions/get-locations.md) | `GET crm/v2/tenant/{{credentials.tenant}}/locations` |  |
| [Get Material by Id](actions/get-material-by-id.md) | `GET pricebook/v2/tenant/{{credentials.tenant}}/materials/:id` |  |
| [Get Materials](actions/get-materials.md) | `GET pricebook/v2/tenant/{{credentials.tenant}}/materials` | [docs](https://developer.servicetitan.io/api-details/#api=tenant-pricebook-v2&operation=Materials_GetList) |
| [Get Payment Types](actions/get-payment-types.md) | `GET accounting/v2/tenant/{{credentials.tenant}}/payment-types` |  |
| [Get Payments](actions/get-payments.md) | `GET accounting/v2/tenant/{{credentials.tenant}}/payments` | [docs](https://developer.servicetitan.io/api-details/#api=tenant-accounting-v2&operation=Payments_GetList) |
| [Get Project](actions/get-project.md) | `GET /jpm/v2/tenant/{{credentials.tenant}}/projects/:id` |  |
| [Get Project Notes](actions/get-project-notes.md) | `GET jpm/v2/tenant/{{credentials.tenant}}/projects/:id/notes` |  |
| [Get Project Statuses](actions/get-project-statuses.md) | `GET https://api.servicetitan.io/jpm/v2/tenant/{{credentials.tenant}}/project-statuses` | [docs](https://developer.servicetitan.io/api-details/#api=tenant-jpm-v2&operation=ProjectStatuses_GetList) |
| [Get Project Sub Statuses](actions/get-project-sub-statuses.md) | `GET https://api.servicetitan.io/jpm/v2/tenant/{{credentials.tenant}}/project-substatuses` | [docs](https://developer.servicetitan.io/api-details/#api=tenant-jpm-v2&operation=ProjectSubStatuses_GetList) |
| [Get Project Types](actions/get-project-types.md) | `GET https://api.servicetitan.io/jpm/v2/tenant/{{credentials.tenant}}/project-types` |  |
| [Get Projects](actions/get-projects.md) | `GET /jpm/v2/tenant/{{credentials.tenant}}/projects` |  |
| [Get Purchase Orders](actions/get-purchase-orders.md) | `GET inventory/v2/tenant/{{credentials.tenant}}/purchase-orders` |  |
| [Get Report](actions/get-report.md) | `GET reporting/v2/tenant/{{credentials.tenant}}/report-category/:report_category/reports/:reportId` | [docs](https://developer.servicetitan.io/docs/apis/tenant-reporting-v2/endpoints/ReportCategoryReports_Get) |
| [Get Report Category Reports](actions/get-report-category-reports.md) | `POST reporting/v2/tenant/{{credentials.tenant}}/report-category/:category/reports/:reportId/data` | [docs](https://developer.servicetitan.io/docs/apis/tenant-forms-v2/endpoints/Jobs_CreateAttachment) |
| [Get Report Data](actions/get-report-data.md) | `POST reporting/v2/tenant/{{credentials.tenant}}/report-category/:report_category/reports/:reportId/data` | [docs](https://developer.servicetitan.io/docs/apis/tenant-reporting-v2/endpoints/ReportCategoryReports_GetData) |
| [Get Returns](actions/get-returns.md) | `GET inventory/v2/tenant/{{credentials.tenant}}/returns` |  |
| [Get Services by Id](actions/get-service-by-id.md) | `GET pricebook/v2/tenant/{{credentials.tenant}}/services/:id` |  |
| [Get Services](actions/get-services.md) | `GET pricebook/v2/tenant/{{credentials.tenant}}/services` |  |
| [Get Tasks](actions/get-tasks.md) | `GET taskmanagement/v2/tenant/{{credentials.tenant}}/tasks` | [docs](https://developer.servicetitan.io/api-details/#api=tenant-task-management-v2&operation=Tasks_GetTasks) |
| [Get Technicians](actions/get-technicians.md) | `GET settings/v2/tenant/{{credentials.tenant}}/technicians` | [docs](https://developer.servicetitan.io/api-details/#api=tenant-settings-v2&operation=Technicians_GetList) |
| [List Vendors](actions/get-vendors.md) | `GET inventory/v2/tenant/{{credentials.tenant}}/vendors` | [docs](https://developer.servicetitan.io/api-details/#api=tenant-inventory-v2&operation=Vendors_GetList) |
| [Get Call Reasons](actions/job-booking-get-call-reasons.md) | `GET jbce/v2/tenant/{{credentials.tenant}}/call-reasons` |  |
| [Get Job](actions/job-planning-get-job.md) | `GET jpm/v2/tenant/{{credentials.tenant}}/jobs/:jobId` |  |
| [Get Jobs](actions/job-planning-get-jobs.md) | `GET https://api.servicetitan.io/jpm/v2/tenant/{{credentials.tenant}}/jobs` | [docs](https://developer.servicetitan.io/api-details/#api=tenant-jpm-v2&operation=Jobs_GetList) |
| [List Activities](actions/list-activities.md) | `GET timesheets/v2/tenant/{{credentials.tenant}}/activities` | [docs](https://developer.servicetitan.io/api-details/#api=tenant-timesheets-v2&operation=ActivitiesControllers_GetList) |
| [List Activity Categories](actions/list-activity-categories.md) | `GET timesheets/v2/tenant/{{credentials.tenant}}/activity-categories` | [docs](https://developer.servicetitan.io/api-details/#api=tenant-timesheets-v2&operation=ActivityTypes_GetList) |
| [List Activity Codes](actions/list-activity-codes.md) | `GET payroll/v2/tenant/{{credentials.tenant}}/activity-codes` | [docs](https://developer.servicetitan.io/api-details/#api=tenant-payroll-v2&operation=Payrolls_GetList) |
| [List Activity Types](actions/list-activity-types.md) | `GET timesheets/v2/tenant/{{credentials.tenant}}/activity-types` | [docs](https://developer.servicetitan.io/api-details/#api=tenant-timesheets-v2&operation=ActivityTypes_GetList) |
| [List Customer Contact](actions/list-customer-contact.md) | `GET crm/v2/tenant/{{credentials.tenant}}/customers/:contactId/contacts` | [docs](https://developer.servicetitan.io/api-details/#api=tenant-crm-v2&operation=Customers_GetContactList) |
| [List Customers Contacts](actions/list-customers-contacts.md) | `GET crm/v2/tenant/{{credentials.tenant}}/customers/contacts` | [docs](https://developer.servicetitan.io/api-details/#api=tenant-crm-v2&operation=Customers_GetContactList) |
| [List Customers With External Data](actions/list-customers-with-external-data.md) | `GET crm/v2/tenant/{{credentials.tenant}}/customers` | [docs](https://developer.servicetitan.io/docs/apis/tenant-crm-v2/endpoints/Customers_GetList) |
| [List Dynamic Set Values](actions/list-dynamic-set-values.md) | `GET reporting/v2/tenant/{{credentials.tenant}}/dynamic-value-sets/:dynamicSetId` | [docs](https://developer.servicetitan.io/docs/apis/tenant-reporting-v2/endpoints/DynamicValueSets_GetDynamicSet) |
| [List Gross Pay Items](actions/list-gross-pay-items.md) | `GET payroll/v2/tenant/{{credentials.tenant}}/gross-pay-items` | [docs](https://developer.servicetitan.io/docs/apis/tenant-payroll-v2/endpoints/GrossPayItems_GetList) |
| [List Inventory Adjustments](actions/list-inventory-adjustments.md) | `GET inventory/v2/tenant/{{credentials.tenant}}/adjustments` | [docs](https://developer.servicetitan.io/api-details/#api=tenant-inventory-v2&operation=Adjustments_GetList) |
| [List Memberships](actions/list-memberships.md) | `GET memberships/v2/tenant/{{credentials.tenant}}/memberships` | [docs](https://developer.servicetitan.io/api-details/#api=tenant-memberships-v2&operation=CustomerMemberships_GetList) |
| [List Non-Job Payroll Timesheets](actions/list-non-job-payroll-timesheets.md) | `GET payroll/v2/tenant/{{credentials.tenant}}/non-job-timesheets` | [docs](https://developer.servicetitan.io/api-details/#api=tenant-payroll-v2&operation=Timesheets_GetNonJobTimesheets) |
| [List Payroll](actions/list-payroll.md) | `GET payroll/v2/tenant/{{credentials.tenant}}/payrolls` | [docs](https://developer.servicetitan.io/api-details/#api=tenant-payroll-v2&operation=Payrolls_GetList) |
| [List Payroll by Employee ID](actions/list-payroll-by-employee-id.md) | `GET payroll/v2/tenant/{{credentials.tenant}}/employees/:employeeID/payrolls` | [docs](https://developer.servicetitan.io/api-details/#api=tenant-payroll-v2&operation=Payrolls_GetList) |
| [List Payroll by Technician ID](actions/list-payroll-by-technician-id.md) | `GET payroll/v2/tenant/{{credentials.tenant}}/technicians/:technicianID/payrolls` | [docs](https://developer.servicetitan.io/api-details/#api=tenant-payroll-v2&operation=Payrolls_GetList) |
| [List Payroll Timesheets](actions/list-payroll-timesheets.md) | `GET payroll/v2/tenant/{{credentials.tenant}}/jobs/timesheets` | [docs](https://developer.servicetitan.io/api-details/#api=tenant-payroll-v2&operation=Timesheets_GetJobTimesheetsByJobs) |
| [List Purchase Order Types](actions/list-purchase-order-types.md) | `GET inventory/v2/tenant/{{credentials.tenant}}/purchase-order-types` | [docs](https://developer.servicetitan.io/api-details/#api=tenant-inventory-v2&operation=PurchaseOrderTypes_GetList) |
| [List Report Categories](actions/list-report-categories.md) | `GET reporting/v2/tenant/{{credentials.tenant}}/report-categories` | [docs](https://developer.servicetitan.io/docs/apis/tenant-reporting-v2/endpoints/ReportCategories_GetCategories) |
| [List Reports](actions/list-reports.md) | `GET reporting/v2/tenant/{{credentials.tenant}}/report-category/:report_category/reports` | [docs](https://developer.servicetitan.io/docs/apis/tenant-reporting-v2/endpoints/ReportCategoryReports_GetReports) |
| [List Timesheet Codes](actions/list-timesheet-codes.md) | `GET payroll/v2/tenant/{{credentials.tenant}}/timesheet-codes` | [docs](https://developer.servicetitan.io/api-details/#api=tenant-payroll-v2&operation=Payrolls_GetList) |
| [Mark AP Bills as Exported](actions/mark-ap-bills-as-exported.md) | `POST accounting/v2/tenant/{{credentials.tenant}}/ap-bills/markasexported` | [docs](https://developer.servicetitan.io/docs/apis/tenant-accounting-v2/endpoints/ApBills_MarkAsExported) |
| [Mark Invoice as Exported](actions/mark-invoice-as-exported.md) | `POST accounting/v2/tenant/{{credentials.tenant}}/invoices/markasexported` | [docs](https://developer.servicetitan.io/api-details/#api=tenant-accounting-v2&operation=Invoices_GetList) |
| [Update Payment Custom Fields](actions/new-action2.md) | `PATCH accounting/v2/tenant/{{credentials.tenant}}/payments/custom-fields` | [docs](https://developer.servicetitan.io/docs/apis/tenant-accounting-v2/endpoints/Payments_UpdateCustomFields) |
| [Add Vendor](actions/post-vendor.md) | `POST inventory/v2/tenant/{{credentials.tenant}}/vendors` | [docs](https://developer.servicetitan.io/api-details/#api=tenant-inventory-v2&operation=Vendors_Create) |
| [Update Costumer](actions/update-costumer.md) | `PATCH crm/v2/tenant/{{credentials.tenant}}/customers/:customerId` |  |
| [Update Customer Membership](actions/update-customer-membership.md) | `PATCH memberships/v2/tenant/{{credentials.tenant}}/memberships/:membershipId` | [docs](https://developer.servicetitan.io/api-details/#api=tenant-memberships-v2&operation=CustomerMemberships_Update) |
| [Update GL Account](actions/update-gl-account.md) | `PATCH accounting/v2/tenant/{{credentials.tenant}}/gl-accounts/:id` |  |
| [Update Job](actions/update-job.md) | `PATCH jpm/v2/tenant/{{credentials.tenant}}/jobs/:jobId` | [docs](https://developer.servicetitan.io/docs/apis/tenant-jpm-v2/endpoints/Jobs_Update) |
| [Update Location Tags](actions/update-location-tags.md) | `PATCH crm/v2/tenant/{{credentials.tenant}}/locations/:id` |  |
| [Update Payment](actions/update-payment.md) | `PATCH accounting/v2/tenant/{{credentials.tenant}}/payments/{{paymentId}}` |  |
| [Update Payment Status](actions/update-payment-status.md) | `POST accounting/v2/tenant/{{credentials.tenant}}/payments/status` |  |
| [Update Vendor](actions/update-vendor.md) | `PATCH inventory/v2/tenant/{{credentials.tenant}}/vendors/:id` |  |
| [Upload Job Attachment](actions/upload-job-attachment.md) | `POST jpm/v2/tenant/{{credentials.tenant}}/jobs/:id/attachments` | [docs](https://developer.servicetitan.io/docs/apis/tenant-forms-v2/endpoints/Jobs_CreateAttachment) |
