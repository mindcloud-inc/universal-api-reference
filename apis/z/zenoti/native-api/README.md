# Zenoti: Native API Reference

A consolidated summary of Zenoti's API configuration and 18 documented operations, with links to official documentation.

- **Official docs:** https://docs.zenoti.com/reference/generate-an-access-token
- **API base URL:** `https://api.zenoti.com/v1/`

## Authentication

### API Token

### Credentials

- **API Key:** `apiKey` · optional

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

The total page count is read from `data.pageInfo.total`.

## Retry behavior

Multiply the delay by 3 after each failed attempt.

## Endpoints (18 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Guest Details](actions/get-guest-details.md) | `GET guests/:guestId` | [docs](https://docs.zenoti.com/reference/retrieve-guest-details) |
| [Get Package Benefits Detail Report](actions/get-package-benefits-detail-report.md) | `POST reports/packages/benefits/flat_file` |  |
| [Get Sales Accrual Report](actions/get-sales-accrual-report.md) | `POST reports/sales/accrual_basis/flat_file` | [docs](None) |
| [List Appointments](actions/list-appointments.md) | `GET appointments` | [docs](https://docs.zenoti.com/reference/retrieve-the-list-of-appointments-of-a-center) |
| [List Appointments By Guest](actions/list-appointments-by-guest.md) | `GET guests/:guestId/appointments` | [docs](https://docs.zenoti.com/reference/list-all-appointments-of-a-guest) |
| [Get Appointments Report](actions/list-appointments-flat-file.md) | `POST reports/appointments/flat_file` | [docs](none) |
| [List Center Blockout Times](actions/list-center-blockout-times.md) | `GET centers/:centerId/blockouttimes` | [docs](https://docs.zenoti.com/reference/list-all-blockout-times-of-a-center) |
| [List Center Employee Schedules](actions/list-center-employee-schedules.md) | `GET centers/:centerId/employee_schedules` | [docs](https://docs.zenoti.com/reference/retrieve-the-schedules-of-employees-of-a-center) |
| [List Center Membership Details](actions/list-center-membership-details.md) | `GET centers/:centerId/members` | [docs](https://docs.zenoti.com/reference/retrieve-the-details-of-all-the-members-of-a-center) |
| [List Centers](actions/list-centers.md) | `GET centers` | [docs](https://docs.zenoti.com/reference/list-all-centers) |
| [Get Collections Report](actions/list-collections.md) | `POST reports/collections/flat_file` | [docs](https://linear.app/mindcloud/issue/MC-1685/create-the-zenoti-app) |
| [List Employees](actions/list-employees.md) | `GET centers/:centerId/employees` | [docs](https://docs.zenoti.com/reference/list-all-employees-of-a-center) |
| [List Guest Memberships](actions/list-guest-memberships.md) | `GET guests/:guestId/memberships` | [docs](https://docs.zenoti.com/reference/list-all-memberships-of-a-guest) |
| [Get Memberships Report](actions/list-memberships.md) | `POST reports/memberships/flat_file` | [docs](None) |
| [List Purchases By Guest](actions/list-purchases-by-guest.md) | `GET guests/:guestId/products` | [docs](https://docs.zenoti.com/reference/list-all-products-purchased-by-a-guest) |
| [Get Sales Report](actions/list-sales.md) | `POST reports/sales/accrual_basis/flat_file` | [docs](None) |
| [List Services](actions/list-services.md) | `GET Centers/:centerId/services` | [docs](https://docs.zenoti.com/reference/list-all-services-of-a-center) |
| [List Therapists](actions/list-therapists.md) | `GET centers/:centerId/therapists` | [docs](https://docs.zenoti.com/reference/list-all-therapists-of-a-center) |
