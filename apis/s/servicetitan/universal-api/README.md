# <img src="https://images.mindcloud.co/apps/icons/service-titan_1777386591371.png" alt="ServiceTitan logo" width="28" height="28"> ServiceTitan: Universal API

ServiceTitan through the MindCloud Universal API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/servicetitan/latest
- **Category:** Support / Field Service
- **Actions:** 97
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor API docs:** https://developer.servicetitan.io/api-details/#api=tenant-crm-v2

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Activity Codes](actions/list-activity-codes.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/list-activity-codes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (97)

### Access Tokens

| Action | Method | Description |
| --- | --- | --- |
| [Get Access Token](actions/get-access-token.md) | GET |  |

### Accounting

| Action | Method | Description |
| --- | --- | --- |
| [Create GL Account](actions/create-gl-account.md) | POST |  |
| [Create Payment](actions/create-payment.md) | POST | Creates a new payment in ServiceTitan. |
| [Get GL Account Types](actions/get-gl-account-types.md) | GET |  |
| [Get GL Accounts](actions/get-gl-accounts.md) | GET |  |
| [Get Payment Types](actions/get-payment-types.md) | GET |  |
| [Get Payments](actions/get-payments.md) | GET | Gets a paginated list of payments |
| [Update GL Account](actions/update-gl-account.md) | PUT |  |
| [Update Payment](actions/update-payment.md) | PUT | Updates an existing payment in ServiceTitan. |
| [Update Payment Status](actions/update-payment-status.md) | PUT | Updates a payment status in ServiceTitan. |

### Appointment

| Action | Method | Description |
| --- | --- | --- |
| [Get Appointment Assignments](actions/get-appointment-assignments.md) | GET |  |
| [Get Appointment by Id](actions/get-appointment-by-id.md) | GET | Retrieves an appointment from ServiceTitan by ID. |
| [Get Appointments](actions/get-appointments.md) | GET |  |

### Booking

| Action | Method | Description |
| --- | --- | --- |
| [Create Booking](actions/create-booking.md) | POST |  |
| [Get Booking Providers](actions/get-booking-providers.md) | GET |  |
| [Get Bookings](actions/get-bookings.md) | GET |  |

### Customer

| Action | Method | Description |
| --- | --- | --- |
| [Create Customer Contact](actions/create-customer-contact.md) | POST | Creates a new customer contact in ServiceTitan. |

### Customers

| Action | Method | Description |
| --- | --- | --- |
| [Create Customer](actions/create-customer.md) | POST | Creates a new customer in ServiceTitan. |
| [Get Customer By Id](actions/get-customer-by-id.md) | GET |  |
| [Get Customers](actions/get-customers.md) | GET |  |
| [List Customer Contact](actions/list-customer-contact.md) | GET | Retrieves contacts from ServiceTitan for a customer. |
| [List Customers Contacts](actions/list-customers-contacts.md) | GET | Retrieves customer contacts from ServiceTitan. |
| [Update Costumer](actions/update-costumer.md) | PUT | Updates an existing customer in ServiceTitan. |

### Discount And Fees

| Action | Method | Description |
| --- | --- | --- |
| [Get Discount and Fees](actions/get-discount-and-fees.md) | GET | Retrieves pricebook discounts and fees from ServiceTitan. |

### Form Submissions

| Action | Method | Description |
| --- | --- | --- |
| [Get Forms Submissions](actions/get-forms-submissions.md) | GET |  |

### Forms

| Action | Method | Description |
| --- | --- | --- |
| [Get Forms](actions/get-forms.md) | GET |  |

### Inventory

| Action | Method | Description |
| --- | --- | --- |
| [Export Adjustments](actions/export-adjustments.md) | GET |  |
| [Export Purchase Orders](actions/export-purchase-orders.md) | GET |  |
| [Export Returns](actions/export-returns.md) | GET |  |
| [Export Transfers](actions/export-transfers.md) | GET |  |
| [Get Item Receipts](actions/get-item-receipts.md) | GET |  |
| [Get Purchase Orders](actions/get-purchase-orders.md) | GET |  |
| [Get Returns](actions/get-returns.md) | GET |  |
| [List Vendors](actions/get-vendors.md) | GET | Retrieves vendors from ServiceTitan. |
| [List Purchase Order Types](actions/list-purchase-order-types.md) | GET | Retrieves purchase order types from ServiceTitan. |
| [Add Vendor](actions/post-vendor.md) | POST |  |
| [Update Vendor](actions/update-vendor.md) | PUT |  |

### Inventory Adjustments

| Action | Method | Description |
| --- | --- | --- |
| [List Inventory Adjustments](actions/list-inventory-adjustments.md) | GET | Retrieves inventory adjustments from ServiceTitan. |

### Invoices

| Action | Method | Description |
| --- | --- | --- |
| [Get Invoices](actions/get-invoices.md) | GET | Retrieves invoices from ServiceTitan. |
| [Get Invoices By Job Id](actions/get-invoices-by-job-id.md) | GET | Retrieves invoices from ServiceTitan by job ID. |
| [Mark Invoice as Exported](actions/mark-invoice-as-exported.md) | PUT | Update Invoice record. |

### Job

| Action | Method | Description |
| --- | --- | --- |
| [Create Job Note](actions/create-job-note.md) | POST |  |
| [Export Job Notes](actions/export-job-notes.md) | GET |  |
| [Get Job Notes](actions/get-job-notes.md) | GET |  |
| [Update Job](actions/update-job.md) | PUT | Updates an existing job in ServiceTitan. |
| [Upload Job Attachment](actions/upload-job-attachment.md) | POST | https://developer.servicetitan.io/docs/apis/tenant-forms-v2/endpoints/Jobs_CreateAttachment |

### Job Booking

| Action | Method | Description |
| --- | --- | --- |
| [Get Call Reasons](actions/job-booking-get-call-reasons.md) | GET |  |

### Job Planning

| Action | Method | Description |
| --- | --- | --- |
| [Create Job](actions/create-job.md) | POST |  |
| [Create Project](actions/create-project.md) | POST |  |
| [Create Project Note](actions/create-project-note.md) | POST |  |
| [Get Job Types](actions/get-job-types.md) | GET |  |
| [Get Projects](actions/get-projects.md) | GET |  |
| [Get Job](actions/job-planning-get-job.md) | GET |  |
| [Get Jobs](actions/job-planning-get-jobs.md) | GET |  |

### Location

| Action | Method | Description |
| --- | --- | --- |
| [Create Location](actions/create-location.md) | POST |  |
| [Get Location By Id](actions/get-location-by-id.md) | GET | Retrieves a location from ServiceTitan by ID. |
| [Get Locations](actions/get-locations.md) | GET |  |

### Marketing

| Action | Method | Description |
| --- | --- | --- |
| [Get Campaigns](actions/get-campaigns.md) | GET | Gets a paginated list of campaigns |

### Membership

| Action | Method | Description |
| --- | --- | --- |
| [Create Customer Membership](actions/create-customer-membership.md) | POST | Creates a customer membership sale in ServiceTitan. |
| [List Memberships](actions/list-memberships.md) | GET | Retrieves customer memberships from ServiceTitan. |
| [Update Customer Membership](actions/update-customer-membership.md) | PUT | Updates an existing customer membership in ServiceTitan. |

### Notes

| Action | Method | Description |
| --- | --- | --- |
| [Get Lead Notes](actions/get-lead-notes.md) | GET | Retrieves lead notes from ServiceTitan. |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Add Customer Tag](actions/add-customer-tag.md) | POST |  |
| [List Payroll by Employee ID](actions/list-payroll-by-employee-id.md) | GET | Retrieves payrolls from ServiceTitan for an employee. |
| [List Payroll by Technician ID](actions/list-payroll-by-technician-id.md) | GET | Retrieves payrolls from ServiceTitan for a technician. |
| [Update Location Tags](actions/update-location-tags.md) | PATCH |  |

### Payroll Runs

| Action | Method | Description |
| --- | --- | --- |
| [List Payroll](actions/list-payroll.md) | GET | Retrieves payrolls from ServiceTitan. |

### Pricebook

| Action | Method | Description |
| --- | --- | --- |
| [Get Equipment by Id](actions/get-equipment-by-id.md) | GET |  |
| [Get Equipments](actions/get-equipments.md) | GET | Retrieves pricebook equipment from ServiceTitan. |
| [Get Material by Id](actions/get-material-by-id.md) | GET |  |
| [Get Materials](actions/get-materials.md) | GET | Retrieves pricebook materials from ServiceTitan. |
| [Get Services by Id](actions/get-service-by-id.md) | GET |  |
| [Get Services](actions/get-services.md) | GET |  |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Export Project Notes](actions/export-project-notes.md) | GET |  |
| [Get Project](actions/get-project.md) | GET |  |
| [Get Project Notes](actions/get-project-notes.md) | GET |  |
| [Get Project Statuses](actions/get-project-statuses.md) | GET | Retrieves project statuses from ServiceTitan. |
| [Get Project Sub Statuses](actions/get-project-sub-statuses.md) | GET | Retrieves project substatuses from ServiceTitan. |
| [Get Project Types](actions/get-project-types.md) | GET |  |

### Reports

| Action | Method | Description |
| --- | --- | --- |
| [Get Report](actions/get-report.md) | GET | Retrieves a report definition from ServiceTitan. |
| [Get Report Data](actions/get-report-data.md) | GET | Retrieves report data from ServiceTitan. |
| [List Dynamic Set Values](actions/list-dynamic-set-values.md) | GET | Retrieves dynamic set values from ServiceTitan. |
| [List Report Categories](actions/list-report-categories.md) | GET | Retrieves report categories from ServiceTitan. |
| [List Reports](actions/list-reports.md) | GET | Retrieves reports from ServiceTitan by category. |

### Settings

| Action | Method | Description |
| --- | --- | --- |
| [Get Business Units](actions/get-business-units.md) | GET |  |
| [Get Employees](actions/get-employees.md) | GET |  |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Create Task](actions/create-task.md) | POST |  |
| [Get Task Management Data](actions/create-task-management-data.md) | GET |  |
| [Get Tasks](actions/get-tasks.md) | GET |  |

### Technician

| Action | Method | Description |
| --- | --- | --- |
| [Get Technicians](actions/get-technicians.md) | GET | Retrieves technicians from ServiceTitan. |

### Timesheets

| Action | Method | Description |
| --- | --- | --- |
| [List Activities](actions/list-activities.md) | GET | Retrieves activities from ServiceTitan. |
| [List Activity Categories](actions/list-activity-categories.md) | GET | Retrieves activity categories from ServiceTitan. |
| [List Activity Codes](actions/list-activity-codes.md) | GET | Retrieves activity codes from ServiceTitan. |
| [List Activity Types](actions/list-activity-types.md) | GET | Retrieves activity types from ServiceTitan. |
| [List Non-Job Payroll Timesheets](actions/list-non-job-payroll-timesheets.md) | GET | Retrieves non-job payroll timesheets from ServiceTitan. |
| [List Payroll Timesheets](actions/list-payroll-timesheets.md) | GET | Retrieves payroll job timesheets from ServiceTitan. |
| [List Timesheet Codes](actions/list-timesheet-codes.md) | GET | Retrieves timesheet codes from ServiceTitan. |

