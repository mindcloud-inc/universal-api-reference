# Trafft: Native API Reference

A consolidated summary of Trafft's API configuration and 10 documented operations, with links to official documentation.

- **Official docs:** https://documenter.getpostman.com/view/1487056/2sAY4x9MRe
- **API base URL:** `https://mindcloud.admin.trafft.com/api/v2`

## Authentication

### Trafft OAuth2 Clean

Clean Trafft OAuth2 client-credentials auth for isolated connection testing.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Exchange the returned authorization code with a POST request to https://mindcloud.admin.trafft.com/api/v2/token.
2. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.


A machine-to-machine flow is configured.

[Official authentication documentation](https://documenter.getpostman.com/view/1487056/2sAY4x9MRe)

## Endpoints (10 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Booking](actions/create-booking.md) | `POST /bookings` | [docs](https://documenter.getpostman.com/view/1487056/2sAY4x9MRe) |
| [Create Customer](actions/create-customer.md) | `POST /customers` | [docs](https://documenter.getpostman.com/view/1487056/2sAY4x9MRe) |
| [Delete Customer](actions/delete-customer.md) | `DELETE /customers/:id` | [docs](https://documenter.getpostman.com/view/1487056/2sAY4x9MRe) |
| [Get Customer by ID](actions/get-customer-by-id.md) | `GET /customers/:id` | [docs](https://documenter.getpostman.com/view/1487056/2sAY4x9MRe) |
| [List Appointments](actions/list-appointments.md) | `GET /appointments` | [docs](https://documenter.getpostman.com/view/1487056/2sAY4x9MRe) |
| [List Customers](actions/list-customers.md) | `GET /customers` | [docs](https://documenter.getpostman.com/view/1487056/2sAY4x9MRe) |
| [List Employees](actions/list-employees.md) | `GET /employees` | [docs](https://documenter.getpostman.com/view/1487056/2sAY4x9MRe) |
| [List Locations](actions/list-locations.md) | `GET /locations` | [docs](https://documenter.getpostman.com/view/1487056/2sAY4x9MRe) |
| [List Services](actions/list-services.md) | `GET /services` | [docs](https://documenter.getpostman.com/view/1487056/2sAY4x9MRe) |
| [Update Customer](actions/update-customer.md) | `PATCH /customers/:id` | [docs](https://documenter.getpostman.com/view/1487056/2sAY4x9MRe) |
