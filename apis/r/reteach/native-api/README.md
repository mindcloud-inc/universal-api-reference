# Reteach: Native API Reference

A consolidated summary of Reteach's API configuration and 21 documented operations, with links to official documentation.

- **Official docs:** https://api.reteach.io/docs/
- **OpenAPI specification:** https://api.reteach.io/docs-json
- **API base URL:** `https://api.reteach.io`

## Authentication

### Reteach App Credentials

Use the client ID, client secret, and client code generated in Reteach Settings > Integrations > API-Zugangsdaten.

### Credentials

- **Client ID:** `clientId` · required · The Reteach client ID generated from the academy API access settings.
- **Client Secret:** `clientSecret` · required · The Reteach client secret generated from the academy API access settings.
- **Client Code:** `clientCode` · required · The Reteach client code generated from the academy API access settings.

Send these headers with each API request:

```http
Authorization: Bearer <custom.accessToken>
```

[Official authentication documentation](https://reteach.notion.site/Rest-API-Access-and-Authentication-eb420cb4a8474b77a6527d19e7db00f2)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 25; minimum 1). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (21 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Course](actions/get-course.md) | `GET /course/{courseId}` | [docs](https://api.reteach.io/docs/#/Course/CourseController_findById) |
| [Get Course Invitation](actions/get-course-invitation.md) | `GET /v1/course-invitation/{courseInvitationId}` | [docs](https://api.reteach.io/docs/#/CourseInvitation/CourseInvitationController_findById) |
| [Get Current Academy](actions/get-current-academy.md) | `GET /me` | [docs](https://api.reteach.io/docs/#/Academy/EditorController_me) |
| [Get Customer](actions/get-customer.md) | `GET /customer/{customerIdentifier}` | [docs](https://api.reteach.io/docs/#/Customer/CustomerController_findCustomerById) |
| [Get Customer Export](actions/get-customer-export.md) | `GET /customer-export/{customerExportId}` | [docs](https://api.reteach.io/docs/#/CustomerExport/CustomerExportController_findCustomerExportById) |
| [Get Customer Group](actions/get-customer-group.md) | `GET /v1/customer-group/{customerGroupId}` | [docs](https://api.reteach.io/docs/#/CustomerGroup/CustomerGroupController_findById) |
| [Get Customer Import](actions/get-customer-import.md) | `GET /customer-import/{customerImportId}` | [docs](https://api.reteach.io/docs/#/CustomerImport/CustomerImportController_findCustomerImportById) |
| [Get E-Commerce Order](actions/get-e-commerce-order.md) | `GET /v1/order/{orderId}` | [docs](https://api.reteach.io/docs/#/Order/ProductVariantOrderController_findById) |
| [Get Participation](actions/get-participation.md) | `GET /participation/{participationId}` | [docs](https://api.reteach.io/docs/#/Participation/CustomerCourseParticipationController_findById) |
| [Get Webhook](actions/get-webhook.md) | `GET /subscription/{subscriptionId}` | [docs](https://api.reteach.io/docs/#/Webhook/RestHookController_findSubscriptionById) |
| [List Course Invitations](actions/list-course-invitations.md) | `GET /v1/course-invitation` | [docs](https://api.reteach.io/docs/#/CourseInvitation/CourseInvitationController_findMany) |
| [List Courses](actions/list-courses.md) | `GET /course` | [docs](https://api.reteach.io/docs/#/Course/CourseController_findManyAndCount) |
| [List Customer Course Certificates](actions/list-customer-course-certificates.md) | `GET /certificates` | [docs](https://api.reteach.io/docs/#/CustomerCourseCertificate/CustomerCourseCertificateController_findManyAndCount) |
| [List Customer Exports](actions/list-customer-exports.md) | `GET /customer-export` | [docs](https://api.reteach.io/docs/#/CustomerExport/CustomerExportController_findCustomerExports) |
| [List Customer Groups](actions/list-customer-groups.md) | `GET /v1/customer-group` | [docs](https://api.reteach.io/docs/#/CustomerGroup/CustomerGroupController_findMany) |
| [List Customer Imports](actions/list-customer-imports.md) | `GET /customer-import` | [docs](https://api.reteach.io/docs/#/CustomerImport/CustomerImportController_findCustomerImports) |
| [List Customers](actions/list-customers.md) | `GET /customer` | [docs](https://api.reteach.io/docs/#/Customer/CustomerController_findCustomer) |
| [List E-Commerce Orders](actions/list-e-commerce-orders.md) | `GET /v1/order` | [docs](https://api.reteach.io/docs/#/Order/ProductVariantOrderController_findManyAndCount) |
| [List Participations](actions/list-participations.md) | `GET /participation` | [docs](https://api.reteach.io/docs/#/Participation/CustomerCourseParticipationController_findMany) |
| [List Tags](actions/list-tags.md) | `GET /tags` | [docs](https://api.reteach.io/docs/#/Tag/TagController_findMany) |
| [List Webhooks](actions/list-webhooks.md) | `GET /subscription` | [docs](https://api.reteach.io/docs/#/Webhook/RestHookController_findSubscriptions) |
