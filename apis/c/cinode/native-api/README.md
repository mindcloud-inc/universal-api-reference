# Cinode: Native API Reference

A consolidated summary of Cinode's API configuration and 22 documented operations, with links to official documentation.

- **Official docs:** https://api.cinode.com/docs/index.html
- **OpenAPI specification:** https://api.cinode.com/swagger/v0.2/swagger.json
- **API base URL:** `https://api.cinode.com`

## Authentication

### Personal API Account

Exchange a Base64 encoded `AccessId:AccessSecret` string for a short-lived bearer token using Cinode's personal API account flow.

### Credentials

- **Encoded Credentials:** `encodedCredentials` · required · Base64 encoded `AccessId:AccessSecret` value used in the Authorization Basic header.

Send these headers with each API request:

```http
Authorization: Bearer <custom.access_token>
```

[Official authentication documentation](https://support.cinode.com/en/articles/91483-rest-api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (22 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Customer Tag](actions/add-customer-tag.md) | `POST /v0.2/companies/:companyId/customers/:customerId/tags` | [docs](https://api.cinode.com/docs/index.html#/CompanyCustomerTags/TagCustomerV02) |
| [Add Project Assignment Tag](actions/add-project-assignment-tag.md) | `POST /v0.2/companies/:companyId/projects/:projectId/roles/:roleId/tags` | [docs](https://api.cinode.com/docs/index.html#/ProjectAssignmentTags/TagProjectAssignment) |
| [Add Project Tag](actions/add-project-tag.md) | `POST /v0.2/companies/:companyId/projects/:projectId/tags` | [docs](https://api.cinode.com/docs/index.html#/ProjectTags/TagProjectV02) |
| [Create Customer](actions/create-customer.md) | `POST /v0.1/companies/:companyId/customers` | [docs](https://api.cinode.com/docs/index.html#/CompanyCustomer/NewCompanyCustomer) |
| [Create Project](actions/create-project.md) | `POST /v0.1/companies/:companyId/projects` | [docs](https://api.cinode.com/docs/index.html#/Project/NewCompanyProject) |
| [Create Tag Type](actions/create-tag-type.md) | `POST /v0.2/companies/:companyId/tag-types` | [docs](https://api.cinode.com/docs/index.html#/TagTypes/CreateTagType) |
| [Delete Tag Type](actions/delete-tag-type.md) | `DELETE /v0.2/companies/:companyId/tag-types/:id` | [docs](https://api.cinode.com/docs/index.html#/TagTypes/DeleteTagType) |
| [Get Access Token](actions/get-access-token.md) | `GET /token` | [docs](https://support.cinode.com/en/articles/91483-rest-api) |
| [Get Current User](actions/get-current-user.md) | `GET /_whoami` | [docs](https://api.cinode.com/docs/index.html#/WhoAmI/WhoAmI) |
| [Get Customer](actions/get-customer.md) | `GET /v0.1/companies/:companyId/customers/:id` | [docs](https://api.cinode.com/docs/index.html#/CompanyCustomer/GetCompanyCustomer) |
| [Get Project](actions/get-project.md) | `GET /v0.1/companies/:companyId/projects/:id` | [docs](https://api.cinode.com/docs/index.html#/Project/Project) |
| [Get Tag Type](actions/get-tag-type.md) | `GET /v0.2/companies/:companyId/tag-types/:id` | [docs](https://api.cinode.com/docs/index.html#/TagTypes/GetTagType) |
| [List Customer Tags](actions/list-customer-tags.md) | `GET /v0.2/companies/:companyId/customers/:customerId/tags` | [docs](https://api.cinode.com/docs/index.html#/CompanyCustomerTags/GetCustomerTagsV02) |
| [List Customers](actions/list-customers.md) | `GET /v0.1/companies/:companyId/customers` | [docs](https://api.cinode.com/docs/index.html#/CompanyCustomers/CompanyCustomers) |
| [List Project Assignment Tags](actions/list-project-assignment-tags.md) | `GET /v0.2/companies/:companyId/projects/:projectId/roles/:roleId/tags` | [docs](https://api.cinode.com/docs/index.html#/ProjectAssignmentTags/GetProjectAssignmentTags) |
| [List Project Tags](actions/list-project-tags.md) | `GET /v0.2/companies/:companyId/projects/:projectId/tags` | [docs](https://api.cinode.com/docs/index.html#/ProjectTags/GetProjectTagsV02) |
| [List Projects](actions/list-projects.md) | `GET /v0.1/companies/:companyId/projects` | [docs](https://api.cinode.com/docs/index.html#/Projects/Projects) |
| [List Tag Types](actions/list-tag-types.md) | `GET /v0.2/companies/:companyId/tag-types` | [docs](https://api.cinode.com/docs/index.html#/TagTypes/GetTagTypes) |
| [Remove Customer Tag](actions/remove-customer-tag.md) | `DELETE /v0.2/companies/:companyId/customers/:customerId/tags/:tagId` | [docs](https://api.cinode.com/docs/index.html#/CompanyCustomerTags/UntagCustomerV02) |
| [Remove Project Assignment Tag](actions/remove-project-assignment-tag.md) | `DELETE /v0.2/companies/:companyId/projects/:projectId/roles/:roleId/tags/:tagId` | [docs](https://api.cinode.com/docs/index.html#/ProjectAssignmentTags/UntagProjectAssignment) |
| [Remove Project Tag](actions/remove-project-tag.md) | `DELETE /v0.2/companies/:companyId/projects/:projectId/tags/:tagId` | [docs](https://api.cinode.com/docs/index.html#/ProjectTags/UntagProjectV02) |
| [Update Tag Type](actions/update-tag-type.md) | `PUT /v0.2/companies/:companyId/tag-types/:id` | [docs](https://api.cinode.com/docs/index.html#/TagTypes/EditTagType) |
