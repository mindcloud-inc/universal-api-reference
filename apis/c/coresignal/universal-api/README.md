# <img src="https://images.mindcloud.co/apps/icons/coresignal-icon_1775762149092.png" alt="Coresignal logo" width="28" height="28"> Coresignal: Universal API

Coresignal provides company, employee, and job intelligence APIs for search, enrichment, and bulk export workflows.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/coresignal/latest
- **Actions:** 48
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://coresignal.com
- **Vendor API docs:** https://docs.coresignal.com

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Collect Base Company By ID](actions/collect-base-company-by-id.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coresignal/latest/actions/collect-base-company-by-id?connectionId=$CONNECTION_ID&companyId=95737800" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (48)

### Company

| Action | Method | Description |
| --- | --- | --- |
| [Collect Base Company By ID](actions/collect-base-company-by-id.md) | GET | Collects a base company from Coresignal by ID. |
| [Collect Clean Company By ID](actions/collect-clean-company-by-id.md) | GET | Collects a clean company from Coresignal by ID. |
| [Collect Clean Company By Identifier](actions/collect-clean-company-by-identifier.md) | GET | Collects a clean company from Coresignal by identifier. |
| [Collect Multi-source Company By ID](actions/collect-multi-source-company-by-id.md) | GET | Collects a multi-source company from Coresignal by ID. |
| [Collect Multi-source Company By Identifier](actions/collect-multi-source-company-by-identifier.md) | GET | Collects a multi-source company from Coresignal by identifier. |
| [Enrich Clean Company](actions/enrich-clean-company.md) | POST | Enriches a clean company in Coresignal. |
| [Enrich Multi-source Company](actions/enrich-multi-source-company.md) | POST | Enriches a multi-source company in Coresignal. |
| [Preview Base Companies By DSL](actions/preview-base-companies-by-dsl.md) | GET | Previews base companies in Coresignal from an Elasticsearch DSL query. |
| [Preview Clean Companies By DSL](actions/preview-clean-companies-by-dsl.md) | GET | Previews clean companies in Coresignal from an Elasticsearch DSL query. |
| [Preview Multi-source Companies By DSL](actions/preview-multi-source-companies-by-dsl.md) | GET | Previews multi-source companies in Coresignal from an Elasticsearch DSL query. |

### Data Request

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Collect Base Companies By DSL](actions/bulk-collect-base-companies-by-dsl.md) | POST | Creates a bulk base company DSL collection request in Coresignal. |
| [Bulk Collect Base Companies By Filters](actions/bulk-collect-base-companies-by-filters.md) | POST | Creates a bulk base company collection request in Coresignal. |
| [Bulk Collect Base Employees By DSL](actions/bulk-collect-base-employees-by-dsl.md) | POST | Creates a bulk base employee DSL collection request in Coresignal. |
| [Bulk Collect Base Employees By Filters](actions/bulk-collect-base-employees-by-filters.md) | POST | Creates a bulk base employee collection request in Coresignal. |
| [Bulk Collect Base Employees By Shorthand Names](actions/bulk-collect-base-employees-by-shorthand-names.md) | POST | Creates a bulk base employee shorthand-name request in Coresignal. |
| [Bulk Collect Base Employees By URLs](actions/bulk-collect-base-employees-by-urls.md) | POST | Creates a bulk base employee URL collection request in Coresignal. |
| [Bulk Collect Base Jobs By Filters](actions/bulk-collect-base-jobs-by-filters.md) | POST | Creates a bulk base job collection request in Coresignal. |
| [Bulk Collect Clean Companies By DSL](actions/bulk-collect-clean-companies-by-dsl.md) | POST | Creates a bulk clean company DSL collection request in Coresignal. |
| [Bulk Collect Clean Companies By IDs](actions/bulk-collect-clean-companies-by-ids.md) | POST | Creates a bulk clean company collection request in Coresignal. |
| [Bulk Collect Clean Companies By Shorthand Names](actions/bulk-collect-clean-companies-by-shorthand-names.md) | POST | Creates a bulk clean company shorthand-name request in Coresignal. |
| [Bulk Collect Clean Companies By URLs](actions/bulk-collect-clean-companies-by-urls.md) | POST | Creates a bulk clean company URL collection request in Coresignal. |
| [Bulk Collect Multi-source Companies By DSL](actions/bulk-collect-multi-source-companies-by-dsl.md) | POST | Creates a bulk multi-source company DSL collection request in Coresignal. |
| [Bulk Collect Multi-source Companies By IDs](actions/bulk-collect-multi-source-companies-by-ids.md) | POST | Creates a bulk multi-source company collection request in Coresignal. |
| [Bulk Collect Multi-source Employees By IDs](actions/bulk-collect-multi-source-employees-by-ids.md) | POST | Creates a bulk multi-source employee collection request in Coresignal. |
| [Bulk Collect Multi-source Jobs By DSL](actions/bulk-collect-multi-source-jobs-by-dsl.md) | POST | Creates a bulk multi-source job DSL collection request in Coresignal. |
| [Bulk Collect Multi-source Jobs By IDs](actions/bulk-collect-multi-source-jobs-by-ids.md) | POST | Creates a bulk multi-source job collection request in Coresignal. |

### Employee

| Action | Method | Description |
| --- | --- | --- |
| [Collect Base Employee By ID](actions/collect-base-employee-by-id.md) | GET | Collects a base employee from Coresignal by ID. |
| [Collect Base Employee By Identifier](actions/collect-base-employee-by-identifier.md) | GET | Collects a base employee from Coresignal by identifier. |
| [Collect Clean Employee By ID](actions/collect-clean-employee-by-id.md) | GET | Collects a clean employee from Coresignal by ID. |
| [Collect Clean Employee By Identifier](actions/collect-clean-employee-by-identifier.md) | GET | Collects a clean employee from Coresignal by identifier. |
| [Collect Multi-source Employee By ID](actions/collect-multi-source-employee-by-id.md) | GET | Collects a multi-source employee from Coresignal by ID. |
| [Collect Multi-source Employee By Identifier](actions/collect-multi-source-employee-by-identifier.md) | GET | Collects a multi-source employee from Coresignal by identifier. |
| [Preview Base Employees By DSL](actions/preview-base-employees-by-dsl.md) | GET | Previews base employees in Coresignal from an Elasticsearch DSL query. |
| [Preview Clean Employees By DSL](actions/preview-clean-employees-by-dsl.md) | GET | Previews clean employees in Coresignal from an Elasticsearch DSL query. |
| [Preview Multi-source Employees By DSL](actions/preview-multi-source-employees-by-dsl.md) | GET | Previews multi-source employees in Coresignal from an Elasticsearch DSL query. |

### File

| Action | Method | Description |
| --- | --- | --- |
| [List Data Request Files](actions/list-data-request-files.md) | GET | Retrieves files for a bulk data request from Coresignal. |

### Job

| Action | Method | Description |
| --- | --- | --- |
| [Collect Base Job By ID](actions/collect-base-job-by-id.md) | GET | Collects a base job from Coresignal by ID. |
| [Collect Multi-source Job By ID](actions/collect-multi-source-job-by-id.md) | GET | Collects a multi-source job from Coresignal by ID. |
| [Preview Base Jobs By DSL](actions/preview-base-jobs-by-dsl.md) | GET | Previews base jobs in Coresignal from an Elasticsearch DSL query. |
| [Preview Multi-source Jobs By DSL](actions/preview-multi-source-jobs-by-dsl.md) | GET | Previews multi-source jobs in Coresignal from an Elasticsearch DSL query. |

### Search Result

| Action | Method | Description |
| --- | --- | --- |
| [Search Base Companies By DSL](actions/search-base-companies-by-dsl.md) | GET | Finds base companies in Coresignal with an Elasticsearch DSL query. |
| [Search Base Employees By DSL](actions/search-base-employees-by-dsl.md) | GET | Finds base employees in Coresignal with an Elasticsearch DSL query. |
| [Search Base Jobs By DSL](actions/search-base-jobs-by-dsl.md) | GET | Finds base jobs in Coresignal with an Elasticsearch DSL query. |
| [Search Clean Companies By DSL](actions/search-clean-companies-by-dsl.md) | GET | Finds clean companies in Coresignal with an Elasticsearch DSL query. |
| [Search Clean Employees By DSL](actions/search-clean-employees-by-dsl.md) | GET | Finds clean employees in Coresignal with an Elasticsearch DSL query. |
| [Search Multi-source Companies By DSL](actions/search-multi-source-companies-by-dsl.md) | GET | Finds multi-source companies in Coresignal with an Elasticsearch DSL query. |
| [Search Multi-source Employees By DSL](actions/search-multi-source-employees-by-dsl.md) | GET | Finds multi-source employees in Coresignal with an Elasticsearch DSL query. |
| [Search Multi-source Jobs By DSL](actions/search-multi-source-jobs-by-dsl.md) | GET | Finds multi-source jobs in Coresignal with an Elasticsearch DSL query. |

