# <img src="https://images.mindcloud.co/apps/icons/one-desk-favicon-144-40x40_1774975959788.png" alt="OneDesk logo" width="28" height="28"> OneDesk: Universal API

Support customers and manage projects in one place with OneDesk's helpdesk, project management, and PSA platform.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/oneDesk/latest
- **Category:** Productivity / Project Management
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://onedesk.com/
- **Vendor API docs:** https://onedesk.com/dev/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Organization Profile And Policy](actions/get-organization-profile-and-policy.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oneDesk/latest/actions/get-organization-profile-and-policy?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Customer

| Action | Method | Description |
| --- | --- | --- |
| [Create Customer](actions/create-customer.md) | POST | Creates a customer in OneDesk. |
| [Get Customer By External ID](actions/get-customer-by-external-id.md) | GET | Retrieves a customer by external ID from OneDesk. |
| [Search Customers](actions/search-customers.md) | GET | Finds customers in OneDesk by filters. |
| [Search Customers With Details](actions/search-customers-with-details.md) | GET | Finds customers in OneDesk by filters, with details. |
| [Update Customer By External ID](actions/update-customer-by-external-id.md) | PUT | Updates a customer in OneDesk by external ID. |

### Customer Organization

| Action | Method | Description |
| --- | --- | --- |
| [Create Customer Organization](actions/create-customer-organization.md) | POST | Creates a customer organization in OneDesk. |
| [Get Customer Organization By External ID](actions/get-customer-organization-by-external-id.md) | GET | Retrieves a customer organization by external ID from OneDesk. |
| [Search Customer Organizations](actions/search-customer-organizations.md) | GET | Finds customer organizations in OneDesk by filters. |
| [Search Customer Organizations With Details](actions/search-customer-organizations-with-details.md) | GET | Finds customer organizations in OneDesk by filters, with details. |
| [Update Customer Organization By External ID](actions/update-customer-organization-by-external-id.md) | PUT | Updates a customer organization in OneDesk by external ID. |

### Organization

| Action | Method | Description |
| --- | --- | --- |
| [Get Organization Lifecycle Status](actions/get-organization-lifecycle-status.md) | GET | Retrieves organization lifecycle status from OneDesk. |
| [Get Organization Profile And Policy](actions/get-organization-profile-and-policy.md) | GET | Retrieves organization profile and policy from OneDesk. |
| [List Organization Container Types](actions/list-organization-container-types.md) | GET | Retrieves organization container types from OneDesk. |
| [List Organization Item Types](actions/list-organization-item-types.md) | GET | Retrieves organization work item types from OneDesk. |
| [List Organization User Types](actions/list-organization-user-types.md) | GET | Retrieves organization user types from OneDesk. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST | Creates a project in OneDesk. |
| [Get Project By External ID](actions/get-project-by-external-id.md) | GET | Retrieves a project by external ID from OneDesk. |
| [Search Projects](actions/search-projects.md) | GET | Finds projects in OneDesk by filters. |
| [Search Projects With Details](actions/search-projects-with-details.md) | GET | Finds projects in OneDesk by filters, with details. |
| [Update Project By External ID](actions/update-project-by-external-id.md) | PUT | Updates a project in OneDesk by external ID. |

