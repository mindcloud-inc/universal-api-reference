# remberg: Native API Reference

A consolidated summary of remberg's API configuration and 45 documented operations, with links to official documentation.

- **Official docs:** https://developers.remberg.de/docs
- **API base URL:** `https://api.remberg.de`

## Authentication

### API Key

Use a remberg API token from the workspace credential settings page. The token is sent as a Bearer token in the Authorization header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developers.remberg.de/docs)

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (45 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Approve Work Request By External Reference](actions/approve-work-request-by-external-reference.md) | `PATCH /v1/work-requests/erp/{externalReference}/approve` | [docs](https://developers.remberg.de/reference/v1work-requestserpexternalreferenceapprove_patch) |
| [Approve Work Request By Id](actions/approve-work-request-by-id.md) | `PATCH /v1/work-requests/{id}/approve` | [docs](https://developers.remberg.de/reference/v1work-requestsidapprove_patch) |
| [Decline Work Request By External Reference](actions/decline-work-request-by-external-reference.md) | `PATCH /v1/work-requests/erp/{externalReference}/decline` | [docs](https://developers.remberg.de/reference/v1work-requestserpexternalreferencedecline_patch) |
| [Decline Work Request By Id](actions/decline-work-request-by-id.md) | `PATCH /v1/work-requests/{id}/decline` | [docs](https://developers.remberg.de/reference/v1work-requestsiddecline_patch) |
| [Delete Asset By Id](actions/delete-asset-by-id.md) | `DELETE /v2/assets/{id}` | [docs](https://developers.remberg.de/reference/v2assetsid_delete) |
| [Delete Asset By Number](actions/delete-asset-by-number.md) | `DELETE /v2/assets/number/{assetNumber}` | [docs](https://developers.remberg.de/reference/v2assetsnumberassetnumber_delete) |
| [Delete Asset Type By Id](actions/delete-asset-type-by-id.md) | `DELETE /v2/assets/types/{id}` | [docs](https://developers.remberg.de/reference/v2assetstypesid_delete) |
| [Delete Asset Type By Label](actions/delete-asset-type-by-label.md) | `DELETE /v2/assets/types/label/{assetTypeLabel}` | [docs](https://developers.remberg.de/reference/v2assetstypeslabelassettypelabel_delete) |
| [Delete Contact By Id](actions/delete-contact-by-id.md) | `DELETE /v1/contacts/{id}` | [docs](https://developers.remberg.de/reference/contactscfacontroller_deleteone) |
| [Delete Organization By Id](actions/delete-organization-by-id.md) | `DELETE /v1/organizations/{id}` | [docs](https://developers.remberg.de/reference/organizationscfacontroller_deleteone) |
| [Delete Ticket By Id](actions/delete-ticket-by-id.md) | `DELETE /v2/tickets/{id}` | [docs](https://developers.remberg.de/reference/v2ticketsid_delete) |
| [Delete Work Order By External Reference](actions/delete-work-order-by-external-reference.md) | `DELETE /v2/work-orders/erp/{externalReference}` | [docs](https://developers.remberg.de/reference/v2work-orderserpexternalreference_delete) |
| [Delete Work Order By Id](actions/delete-work-order-by-id.md) | `DELETE /v2/work-orders/{id}` | [docs](https://developers.remberg.de/reference/v2work-ordersid_delete) |
| [Delete Work Request By External Reference](actions/delete-work-request-by-external-reference.md) | `DELETE /v1/work-requests/erp/{externalReference}` | [docs](https://developers.remberg.de/reference/v1work-requestserpexternalreference_delete) |
| [Delete Work Request By Id](actions/delete-work-request-by-id.md) | `DELETE /v1/work-requests/{id}` | [docs](https://developers.remberg.de/reference/v1work-requestsid_delete) |
| [Download File](actions/download-file.md) | `GET /v1/files/{id}/download` | [docs](https://developers.remberg.de/reference/v1filesiddownload_get) |
| [Get Asset By Id](actions/get-asset-by-id.md) | `GET /v2/assets/{id}` | [docs](https://developers.remberg.de/reference/v2assetsid_get) |
| [Get Asset By Number](actions/get-asset-by-number.md) | `GET /v2/assets/number/{assetNumber}` | [docs](https://developers.remberg.de/reference/v2assetsnumberassetnumber_get) |
| [Get Asset Type By Id](actions/get-asset-type-by-id.md) | `GET /v2/assets/types/{id}` | [docs](https://developers.remberg.de/reference/v2assetstypesid_get) |
| [Get Asset Type By Label](actions/get-asset-type-by-label.md) | `GET /v2/assets/types/label/{assetTypeLabel}` | [docs](https://developers.remberg.de/reference/v2assetstypeslabelassettypelabel_get) |
| [Get Contact By Id](actions/get-contact-by-id.md) | `GET /v1/contacts/{id}` | [docs](https://developers.remberg.de/reference/contactscfacontroller_findone) |
| [Get Failure Types](actions/get-failure-types.md) | `GET /v2/failure-types` | [docs](https://developers.remberg.de/reference/v2failure-types_get) |
| [Get File By Id](actions/get-file-by-id.md) | `GET /v1/files/{id}` | [docs](https://developers.remberg.de/reference/v1filesid_get) |
| [Get Form By Id](actions/get-form-by-id.md) | `GET /v1/forms/{id}` | [docs](https://developers.remberg.de/reference/v1formsid_get) |
| [Get Organization By Id](actions/get-organization-by-id.md) | `GET /v1/organizations/{id}` | [docs](https://developers.remberg.de/reference/organizationscfacontroller_findone) |
| [Get Ticket By Id](actions/get-ticket-by-id.md) | `GET /v2/tickets/{id}` | [docs](https://developers.remberg.de/reference/v2ticketsid_get) |
| [Get Ticket Categories](actions/get-ticket-categories.md) | `GET /v2/tickets/categories` | [docs](https://developers.remberg.de/reference/v2ticketscategories_get) |
| [Get Ticket Conversations](actions/get-ticket-conversations.md) | `GET /v2/tickets/{id}/conversations` | [docs](https://developers.remberg.de/reference/v2ticketsidconversations_get) |
| [Get Work Order By External Reference](actions/get-work-order-by-external-reference.md) | `GET /v2/work-orders/erp/{externalReference}` | [docs](https://developers.remberg.de/reference/v2work-orderserpexternalreference_get) |
| [Get Work Order By Id](actions/get-work-order-by-id.md) | `GET /v2/work-orders/{id}` | [docs](https://developers.remberg.de/reference/v2work-ordersid_get) |
| [Get Work Order Stock Changes By External Reference](actions/get-work-order-stock-changes-by-external-reference.md) | `GET /v2/work-orders/erp/{externalReference}/stock-changes` | [docs](https://developers.remberg.de/reference/v2work-orderserpexternalreferencestock-changes_get) |
| [Get Work Order Stock Changes By Id](actions/get-work-order-stock-changes-by-id.md) | `GET /v2/work-orders/{id}/stock-changes` | [docs](https://developers.remberg.de/reference/v2work-ordersidstock-changes_get) |
| [Get Work Order Time Entries](actions/get-work-order-time-entries.md) | `GET /v2/work-orders/{id}/times` | [docs](https://developers.remberg.de/reference/v2work-ordersidtimes_get) |
| [Get Work Request By External Reference](actions/get-work-request-by-external-reference.md) | `GET /v1/work-requests/erp/{externalReference}` | [docs](https://developers.remberg.de/reference/v1work-requestserpexternalreference_get) |
| [Get Work Request By Id](actions/get-work-request-by-id.md) | `GET /v1/work-requests/{id}` | [docs](https://developers.remberg.de/reference/v1work-requestsid_get) |
| [List Assets](actions/list-assets.md) | `GET /v2/assets` | [docs](https://developers.remberg.de/reference/v2assets_get) |
| [List Contacts](actions/list-contacts.md) | `GET /v1/contacts` | [docs](https://developers.remberg.de/reference/contactscfacontroller_findmany) |
| [List Files](actions/list-files.md) | `GET /v1/files` | [docs](https://developers.remberg.de/reference/v1files_get) |
| [List Forms](actions/list-forms.md) | `GET /v1/forms` | [docs](https://developers.remberg.de/reference/v1forms_get) |
| [List Organization Contacts](actions/list-organization-contacts.md) | `GET /v1/organizations/{id}/contacts` | [docs](https://developers.remberg.de/reference/organizationscfacontroller_findmanycontacts) |
| [List Organizations](actions/list-organizations.md) | `GET /v1/organizations` | [docs](https://developers.remberg.de/reference/organizationscfacontroller_findmany) |
| [List Tickets](actions/list-tickets.md) | `GET /v2/tickets` | [docs](https://developers.remberg.de/reference/v2tickets_get) |
| [List Work Orders](actions/list-work-orders.md) | `GET /v2/work-orders` | [docs](https://developers.remberg.de/reference/v2work-orders_get) |
| [List Work Requests](actions/list-work-requests.md) | `GET /v1/work-requests` | [docs](https://developers.remberg.de/reference/v1work-requests_get) |
| [Resolve File Path](actions/resolve-file-path.md) | `GET /v1/files/resolve` | [docs](https://developers.remberg.de/reference/v1filesresolve_get) |
