# Alto: Native API Reference

A consolidated summary of Alto's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://developers.vebraalto.com/api
- **OpenAPI specification:** https://api.alto.zoopla.co.uk/MergedDocs
- **API base URL:** `https://api.alto.zoopladev.co.uk`

## Authentication

### OAuth2 Client Credentials

Use Alto client credentials to request a bearer token from the Alto Token API, then send the bearer token and AgencyRef header on API requests.

### Credentials

- **Agency Ref:** `agencyRef` · required · AgencyRef issued for the Alto integration. Sent as the AgencyRef header on Alto API requests.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Exchange the returned authorization code with a POST request to https://api.alto.zoopladev.co.uk/token.
2. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.


A machine-to-machine flow is configured.

[Official authentication documentation](https://developers.vebraalto.com/guides/authenticating-your-requests/)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `max-results` in the query string to set the page size (default 100; accepted range 1–100). Use `next-token` in the query string as the pagination cursor.

## Filtering

Send filters in the query string.

## Sorting

Set the sort field with `sort-by` in the query string. Set the direction separately with `sort-order`. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Filter Inventory](actions/filter-inventory.md) | `GET /inventory/filter` | [docs](https://developers.vebraalto.com/api) |
| [Filter Listings](actions/filter-listings.md) | `GET /listing/filter` | [docs](https://developers.vebraalto.com/api) |
| [Get All Contacts](actions/get-all-contacts.md) | `GET /contacts/all` | [docs](https://developers.vebraalto.com/api) |
| [Get Appointment](actions/get-appointment.md) | `GET /appointments/:appointmentId/:instanceId` | [docs](https://developers.vebraalto.com/api) |
| [Get Branch](actions/get-branch.md) | `GET /branches/:branchId` | [docs](https://developers.vebraalto.com/api) |
| [Get Branches](actions/get-branches.md) | `GET /branches` | [docs](https://developers.vebraalto.com/api) |
| [Get Contact](actions/get-contact.md) | `GET /contacts/:contactId` | [docs](https://developers.vebraalto.com/api) |
| [Get Contact Marketing Preferences](actions/get-contact-marketing-preferences.md) | `GET /contacts/:contactId/preferences` | [docs](https://developers.vebraalto.com/api) |
| [Get Contact Person](actions/get-contact-person.md) | `GET /contacts/:contactId/persons/:personId` | [docs](https://developers.vebraalto.com/api) |
| [Get Contact Persons](actions/get-contact-persons.md) | `GET /contacts/:contactId/persons` | [docs](https://developers.vebraalto.com/api) |
| [Get Contact Relationships](actions/get-contact-relationships.md) | `GET /contacts/:contactId/relationship` | [docs](https://developers.vebraalto.com/api) |
| [Get Contacts](actions/get-contacts.md) | `GET /contacts` | [docs](https://developers.vebraalto.com/api) |
| [Get Document Content](actions/get-document-content.md) | `GET /documents/:documentId/content` | [docs](https://developers.vebraalto.com/api) |
| [Get Documents](actions/get-documents.md) | `GET /documents` | [docs](https://developers.vebraalto.com/api) |
| [Get Inventory](actions/get-inventory.md) | `GET /inventory` | [docs](https://developers.vebraalto.com/api) |
| [Get Inventory Documents](actions/get-inventory-documents.md) | `GET /inventory/:inventoryId/documents` | [docs](https://developers.vebraalto.com/api) |
| [Get Inventory Item](actions/get-inventory-item.md) | `GET /inventory/:inventoryId` | [docs](https://developers.vebraalto.com/api) |
| [Get Inventory Items](actions/get-inventory-items.md) | `GET /inventory/items` | [docs](https://developers.vebraalto.com/api) |
| [Get Inventory Landlords](actions/get-inventory-landlords.md) | `GET /inventory/:inventoryId/landlords` | [docs](https://developers.vebraalto.com/api) |
| [Get Inventory Tenancies](actions/get-inventory-tenancies.md) | `GET /inventory/:inventoryId/tenancies` | [docs](https://developers.vebraalto.com/api) |
| [Get Landlords](actions/get-landlords.md) | `GET /landlords` | [docs](https://developers.vebraalto.com/api) |
| [Get Lead](actions/get-lead.md) | `GET /leads/:leadId` | [docs](https://developers.vebraalto.com/api) |
| [Get Leads](actions/get-leads.md) | `GET /leads` | [docs](https://developers.vebraalto.com/api) |
| [Get Negotiator](actions/get-negotiator.md) | `GET /negotiators/:negotiatorId` | [docs](https://developers.vebraalto.com/api) |
| [Get Negotiator Appointments](actions/get-negotiator-appointments.md) | `GET /appointments/negotiators` | [docs](https://developers.vebraalto.com/api) |
| [Get Negotiators](actions/get-negotiators.md) | `GET /negotiators` | [docs](https://developers.vebraalto.com/api) |
| [Get Owners](actions/get-owners.md) | `GET /owners` | [docs](https://developers.vebraalto.com/api) |
| [Get Property Listing](actions/get-property-listing.md) | `GET /listing/property/:propertyId` | [docs](https://developers.vebraalto.com/api) |
| [Get Property Listing Images](actions/get-property-listing-images.md) | `GET /listing/property/:propertyId/images` | [docs](https://developers.vebraalto.com/api) |
| [Get Property Listings](actions/get-property-listings.md) | `GET /listing/property/items` | [docs](https://developers.vebraalto.com/api) |
| [Get Supplier](actions/get-supplier.md) | `GET /suppliers/:supplierId` | [docs](https://developers.vebraalto.com/api) |
| [Get Suppliers](actions/get-suppliers.md) | `GET /suppliers` | [docs](https://developers.vebraalto.com/api) |
| [Get Tenancies](actions/get-tenancies.md) | `GET /tenancies` | [docs](https://developers.vebraalto.com/api) |
| [Get Tenancy](actions/get-tenancy.md) | `GET /tenancies/:tenancyId` | [docs](https://developers.vebraalto.com/api) |
| [Get Tenancy Meter Readings](actions/get-tenancy-meter-readings.md) | `GET /tenancies/:tenancyId/meter-readings` | [docs](https://developers.vebraalto.com/api) |
| [Get Tenancy Tenant IDs](actions/get-tenancy-tenant-ids.md) | `GET /tenancies/:tenancyId/tenantIds` | [docs](https://developers.vebraalto.com/api) |
| [Get Valuations](actions/get-valuations.md) | `GET /appointments/valuations` | [docs](https://developers.vebraalto.com/api) |
| [Get Work Order](actions/get-work-order.md) | `GET /work-orders/:id` | [docs](https://developers.vebraalto.com/api) |
| [Search Contacts](actions/search-contacts.md) | `GET /contacts/search` | [docs](https://developers.vebraalto.com/api) |
| [Search Inventory](actions/search-inventory.md) | `GET /inventory/search` | [docs](https://developers.vebraalto.com/api) |
