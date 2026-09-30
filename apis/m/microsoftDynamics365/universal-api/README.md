# <img src="https://images.mindcloud.co/apps/icons/image-2846-vectorized_1782232770557.png" alt="Microsoft Dynamics 365 logo" width="28" height="28"> Microsoft Dynamics 365: Universal API

Microsoft Dynamics 365 through the MindCloud Universal API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/microsoftDynamics365/latest
- **Actions:** 36
- **OpenAPI specification:** [openapi.json](openapi.json)

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Accounts](actions/get-accounts.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoftDynamics365/latest/actions/get-accounts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (36)

### Companies

| Action | Method | Description |
| --- | --- | --- |
| [Get Accounts](actions/get-accounts.md) | GET |  |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Create Account](actions/create-account.md) | POST |  |
| [Create Contact](actions/create-contact.md) | POST |  |
| [Get Contact By Id](actions/get-contact-by-id.md) | GET |  |
| [Get Contacts](actions/get-contacts.md) | GET |  |
| [Get System Users](actions/get-system-users.md) | GET |  |
| [Patch Accounts](actions/patch-accounts.md) | POST |  |
| [Patch Contact](actions/patch-contact.md) | POST |  |
| [Patch Custom Table Field](actions/patch-custom-table-field.md) | POST |  |

### Customers

| Action | Method | Description |
| --- | --- | --- |
| [Create Customer](actions/create-customer.md) | POST |  |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Create Custom Entity](actions/create-custom-entity.md) | POST |  |
| [Create Customer Postal Address](actions/create-customer-postal-address.md) | POST |  |
| [Create Distinct Product](actions/create-distinct-product.md) | POST |  |
| [Create ProductsV2 Entity](actions/create-products-v2-entity.md) | POST |  |
| [Create Project](actions/create-project.md) | POST |  |
| [Create Project Contract](actions/create-project-contract.md) | POST |  |
| [Create Project Sales Item Requirement](actions/create-project-sales-item-requirement.md) | POST |  |
| [Create Sellable Released Product](actions/create-sellable-released-product.md) | POST |  |
| [Create WBS Activity Estimate](actions/create-wbs-activity-estimate.md) | POST |  |
| [Create WBS Draft Entity](actions/create-wbs-draft-entity.md) | POST |  |
| [Get All Available Entities](actions/get-all-available-entities.md) | GET |  |
| [Get Custom APIs](actions/get-custom-ap-is.md) | GET |  |
| [Get Custom Table](actions/get-custom-table.md) | GET |  |
| [Get Custom Table Entry By Id](actions/get-custom-table-entry-by-id.md) | GET |  |
| [Get Customers](actions/get-customers.md) | GET |  |
| [Get Distinct Products](actions/get-distinct-products.md) | GET |  |
| [Get Logistics Postal Address BI Entities](actions/get-logistics-postal-address-bi-entities.md) | GET |  |
| [Get ProductsV2](actions/get-products-v2.md) | GET |  |
| [Get Project Contracts](actions/get-project-contracts.md) | GET |  |
| [Get Projects](actions/get-projects.md) | GET |  |
| [Get Released Products V2](actions/get-released-products-v2.md) | GET |  |
| [Get Sellable Released Products](actions/get-sellable-released-products.md) | GET |  |
| [Get Trv Exp Mobile Activities](actions/get-trv-exp-mobile-activities.md) | GET |  |
| [Get Workers](actions/get-workers.md) | GET |  |
| [Patch Custom Table](actions/patch-custom-table.md) | PUT |  |
| [Search Entity Definition](actions/search-entity-definition.md) | GET |  |

