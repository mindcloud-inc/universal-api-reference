# OneDesk: Native API Reference

A consolidated summary of OneDesk's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://onedesk.com/dev/
- **OpenAPI specification:** https://onedesk.com/public-api/onedesk-public-api.json
- **API base URL:** `https://app.onedesk.com`

## Authentication

### API Key

Authenticate with a OneDesk public API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
OD-Public-API-Key: <apiKey>
```

[Official authentication documentation](https://onedesk.com/new-api-2024/)

## API conventions

Responses from this API use JSON.

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Customer](actions/create-customer.md) | `POST /rest/public/customers/` | [docs](https://onedesk.com/public-api/swagger.html) |
| [Create Customer Organization](actions/create-customer-organization.md) | `POST /rest/public/customer-organizations/` | [docs](https://onedesk.com/public-api/swagger.html) |
| [Create Project](actions/create-project.md) | `POST /rest/public/projects/` | [docs](https://onedesk.com/public-api/swagger.html) |
| [Get Customer By External ID](actions/get-customer-by-external-id.md) | `GET /rest/public/customers/externalId/:externalId` | [docs](https://onedesk.com/public-api/swagger.html) |
| [Get Customer Organization By External ID](actions/get-customer-organization-by-external-id.md) | `GET /rest/public/customer-organizations/externalId/:externalId` | [docs](https://onedesk.com/public-api/swagger.html) |
| [Get Organization Lifecycle Status](actions/get-organization-lifecycle-status.md) | `GET /rest/public/organization/lifecycleStatus` | [docs](https://onedesk.com/public-api/swagger.html) |
| [Get Organization Profile And Policy](actions/get-organization-profile-and-policy.md) | `GET /rest/public/organization/profileAndPolicy` | [docs](https://onedesk.com/public-api/swagger.html) |
| [Get Project By External ID](actions/get-project-by-external-id.md) | `GET /rest/public/projects/externalId/:externalId` | [docs](https://onedesk.com/public-api/swagger.html) |
| [List Organization Container Types](actions/list-organization-container-types.md) | `GET /rest/public/organization/containerTypes` | [docs](https://onedesk.com/public-api/swagger.html) |
| [List Organization Item Types](actions/list-organization-item-types.md) | `GET /rest/public/organization/itemTypes` | [docs](https://onedesk.com/public-api/swagger.html) |
| [List Organization User Types](actions/list-organization-user-types.md) | `GET /rest/public/organization/userTypes` | [docs](https://onedesk.com/public-api/swagger.html) |
| [Search Customer Organizations](actions/search-customer-organizations.md) | `POST /rest/public/customer-organizations/filter` | [docs](https://onedesk.com/public-api/swagger.html) |
| [Search Customer Organizations With Details](actions/search-customer-organizations-with-details.md) | `POST /rest/public/customer-organizations/filter/details` | [docs](https://onedesk.com/public-api/swagger.html) |
| [Search Customers](actions/search-customers.md) | `POST /rest/public/customers/filter` | [docs](https://onedesk.com/public-api/swagger.html) |
| [Search Customers With Details](actions/search-customers-with-details.md) | `POST /rest/public/customers/filter/details` | [docs](https://onedesk.com/public-api/swagger.html) |
| [Search Projects](actions/search-projects.md) | `POST /rest/public/projects/filter` | [docs](https://onedesk.com/public-api/swagger.html) |
| [Search Projects With Details](actions/search-projects-with-details.md) | `POST /rest/public/projects/filter/details` | [docs](https://onedesk.com/public-api/swagger.html) |
| [Update Customer By External ID](actions/update-customer-by-external-id.md) | `POST /rest/public/customers/externalId/:externalId` | [docs](https://onedesk.com/public-api/swagger.html) |
| [Update Customer Organization By External ID](actions/update-customer-organization-by-external-id.md) | `POST /rest/public/customer-organizations/externalId/:externalId` | [docs](https://onedesk.com/public-api/swagger.html) |
| [Update Project By External ID](actions/update-project-by-external-id.md) | `POST /rest/public/projects/externalId/:externalId` | [docs](https://onedesk.com/public-api/swagger.html) |
