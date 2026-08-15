# ServiceTitan Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model ServiceTitan expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/get-appointment-assignments?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## ServiceTitan actions that support pagination

- [Create Customer](actions/create-customer.md)
- [Get Appointment Assignments](actions/get-appointment-assignments.md)
- [Get Appointments](actions/get-appointments.md)
- [Get Bookings](actions/get-bookings.md)
- [Get Business Units](actions/get-business-units.md)
- [Get Campaigns](actions/get-campaigns.md)
- [Get Customer By Id](actions/get-customer-by-id.md)
- [Get Customers](actions/get-customers.md)
- [Get Discount and Fees](actions/get-discount-and-fees.md)
- [Get Employees](actions/get-employees.md)
- [Get Equipments](actions/get-equipments.md)
- [Get Invoices](actions/get-invoices.md)
- [Get Invoices By Job Id](actions/get-invoices-by-job-id.md)
- [Get Item Receipts](actions/get-item-receipts.md)
- [Get Job Types](actions/get-job-types.md)
- [Get Locations](actions/get-locations.md)
- [Get Materials](actions/get-materials.md)
- [Get Payment Types](actions/get-payment-types.md)
- [Get Payments](actions/get-payments.md)
- [Get Project](actions/get-project.md)
- [Get Project Statuses](actions/get-project-statuses.md)
- [Get Project Sub Statuses](actions/get-project-sub-statuses.md)
- [Get Project Types](actions/get-project-types.md)
- [Get Projects](actions/get-projects.md)
- [Get Purchase Orders](actions/get-purchase-orders.md)
- [Get Report Data](actions/get-report-data.md)
- [Get Returns](actions/get-returns.md)
- [Get Services by Id](actions/get-service-by-id.md)
- [Get Services](actions/get-services.md)
- [Get Tasks](actions/get-tasks.md)
- [Get Technicians](actions/get-technicians.md)
- [List Vendors](actions/get-vendors.md)
- [Get Call Reasons](actions/job-booking-get-call-reasons.md)
- [Get Jobs](actions/job-planning-get-jobs.md)
- [List Activities](actions/list-activities.md)
- [List Customer Contact](actions/list-customer-contact.md)
- [List Customers Contacts](actions/list-customers-contacts.md)
- [List Customers With External Data](actions/list-customers-with-external-data.md)
- [List Dynamic Set Values](actions/list-dynamic-set-values.md)
- [List Gross Pay Items](actions/list-gross-pay-items.md)
- [List Memberships](actions/list-memberships.md)
- [List Payroll](actions/list-payroll.md)
- [List Purchase Order Types](actions/list-purchase-order-types.md)
- [List Report Categories](actions/list-report-categories.md)
- [List Reports](actions/list-reports.md)
- [Update Costumer](actions/update-costumer.md)
