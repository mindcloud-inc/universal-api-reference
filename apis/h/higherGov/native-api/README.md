# HigherGov: Native API Reference

A consolidated summary of HigherGov's API configuration and 19 documented operations, with links to official documentation.

- **Official docs:** https://docs.highergov.com/import-and-export/api
- **OpenAPI specification:** https://www.highergov.com/api-external/schema/
- **API base URL:** `https://www.highergov.com`

## Authentication

### API Key

Authenticate HigherGov API requests with an API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.highergov.com/import-and-export/api)

## API conventions

Response data is read from `results`. The total page count is read from `num_pages`. The current page number is read from `page_number`.

## Pagination

Use `page_size` in the query string to set the page size (default 10; accepted range 1–100). Use `page_number` in the query string to choose the page; numbering starts at 1.

## Sorting

Set the sort field with `ordering` in the query string. Prefix the field name to select its direction. Only one sort field is accepted.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (19 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [List Agencies](actions/list-agencies.md) | `GET /api-external/agency/` | [docs](https://www.highergov.com/api-external/docs/#/api-external/api_external_agency_list) |
| [List Awardee Partnerships](actions/list-awardee-partnerships.md) | `GET /api-external/awardee-partnership/` | [docs](https://www.highergov.com/api-external/docs/#/api-external/api_external_awardee_partnership_list) |
| [List Awardees](actions/list-awardees.md) | `GET /api-external/awardee/` | [docs](https://www.highergov.com/api-external/docs/#/api-external/api_external_awardee_list) |
| [List Contract Vehicles](actions/list-contract-vehicles.md) | `GET /api-external/vehicle/` | [docs](https://www.highergov.com/api-external/docs/#/api-external/api_external_vehicle_list) |
| [List Federal Contracts](actions/list-federal-contracts.md) | `GET /api-external/contract/` | [docs](https://www.highergov.com/api-external/docs/#/api-external/api_external_contract_list) |
| [List Federal Grants](actions/list-federal-grants.md) | `GET /api-external/grant/` | [docs](https://www.highergov.com/api-external/docs/#/api-external/api_external_grant_list) |
| [List Grant Programs](actions/list-grant-programs.md) | `GET /api-external/grant-program/` | [docs](https://www.highergov.com/api-external/docs/#/api-external/api_external_grant_program_list) |
| [List IDV Awards](actions/list-idv-awards.md) | `GET /api-external/idv/` | [docs](https://www.highergov.com/api-external/docs/#/api-external/api_external_idv_list) |
| [List Mentor Protege Relationships](actions/list-mentor-protege-relationships.md) | `GET /api-external/awardee-mp/` | [docs](https://www.highergov.com/api-external/docs/#/api-external/api_external_awardee_mp_list) |
| [List NAICS Codes](actions/list-naics-codes.md) | `GET /api-external/naics/` | [docs](https://www.highergov.com/api-external/docs/#/api-external/api_external_naics_list) |
| [List NSNs](actions/list-nsns.md) | `GET /api-external/nsn/` | [docs](https://www.highergov.com/api-external/docs/#/api-external/api_external_nsn_list) |
| [List Opportunities](actions/list-opportunities.md) | `GET /api-external/opportunity/` | [docs](https://www.highergov.com/api-external/docs/#/api-external/api_external_opportunity_list) |
| [List Opportunity Documents](actions/list-opportunity-documents.md) | `GET /api-external/document/` | [docs](https://www.highergov.com/api-external/docs/#/api-external/api_external_document_list) |
| [List People](actions/list-people.md) | `GET /api-external/people/` | [docs](https://www.highergov.com/api-external/docs/#/api-external/api_external_people_list) |
| [List PSC Codes](actions/list-psc-codes.md) | `GET /api-external/psc/` | [docs](https://www.highergov.com/api-external/docs/#/api-external/api_external_psc_list) |
| [List Pursuits](actions/list-pursuits.md) | `GET /api-external/pursuit/` | [docs](https://www.highergov.com/api-external/docs/#/api-external/api_external_pursuit_list) |
| [List State And Local Contracts](actions/list-state-and-local-contracts.md) | `GET /api-external/sl-contract/` | [docs](https://www.highergov.com/api-external/docs/#/api-external/api_external_sl_contract_list) |
| [List Subcontracts](actions/list-subcontracts.md) | `GET /api-external/subcontract/` | [docs](https://www.highergov.com/api-external/docs/#/api-external/api_external_subcontract_list) |
| [List Subgrants](actions/list-subgrants.md) | `GET /api-external/subgrant/` | [docs](https://www.highergov.com/api-external/docs/#/api-external/api_external_subgrant_list) |
