# Bedrijfsdata.nl: Native API Reference

A consolidated summary of Bedrijfsdata.nl's API configuration and 31 documented operations, with links to official documentation.

- **Official docs:** https://www.postman.com/bedrijfsdatanl/bedrijfsdata-nl-api/overview
- **API base URL:** `https://fapi.bedrijfsdata.nl/v1.2`

## Authentication

### API Key

Use your Bedrijfsdata.nl API key. The runtime sends it in the x-api-key header for every request.

### Credentials

- **API Key:** `apiKey` · required · Your Bedrijfsdata.nl API key.

Send these headers with each API request:

```http
x-api-key: <apiKey>
```

[Official authentication documentation](https://www.postman.com/bedrijfsdatanl/bedrijfsdata-nl-api/collection/rz54v2q/bedrijfsdata-nl-api)

## Endpoints (31 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Check Password Exposure](actions/check-password-exposure.md) | `GET /password` | [docs](https://www.postman.com/bedrijfsdatanl/bedrijfsdata-nl-api/collection/rz54v2q/bedrijfsdata-nl-api) |
| [Enrich Company](actions/enrich-company.md) | `GET /enrich` | [docs](https://www.postman.com/bedrijfsdatanl/bedrijfsdata-nl-api/collection/rz54v2q/bedrijfsdata-nl-api) |
| [Find Companies At Shared Address](actions/find-companies-at-shared-address.md) | `GET /shared_address` | [docs](https://www.postman.com/bedrijfsdatanl/bedrijfsdata-nl-api/collection/rz54v2q/bedrijfsdata-nl-api) |
| [Find Company News](actions/find-company-news.md) | `GET /news` | [docs](https://www.postman.com/bedrijfsdatanl/bedrijfsdata-nl-api/collection/rz54v2q/bedrijfsdata-nl-api) |
| [Find Company People](actions/find-company-people.md) | `GET /people` | [docs](https://www.postman.com/bedrijfsdatanl/bedrijfsdata-nl-api/collection/rz54v2q/bedrijfsdata-nl-api) |
| [Find Company Vacancies](actions/find-company-vacancies.md) | `GET /vacancies` | [docs](https://www.postman.com/bedrijfsdatanl/bedrijfsdata-nl-api/collection/rz54v2q/bedrijfsdata-nl-api) |
| [Geocode Address](actions/geocode-address.md) | `GET /geocoding` | [docs](https://www.postman.com/bedrijfsdatanl/bedrijfsdata-nl-api/collection/rz54v2q/bedrijfsdata-nl-api) |
| [Get Corporate Family](actions/get-corporate-family.md) | `GET /corporate_family` | [docs](https://www.postman.com/bedrijfsdatanl/bedrijfsdata-nl-api/collection/rz54v2q/bedrijfsdata-nl-api) |
| [Get Site Rank Metrics](actions/get-site-rank-metrics.md) | `GET /siterank` | [docs](https://www.postman.com/bedrijfsdatanl/bedrijfsdata-nl-api/collection/rz54v2q/bedrijfsdata-nl-api) |
| [Get Web Rank Summary](actions/get-web-rank-summary.md) | `GET /webrank` | [docs](https://www.postman.com/bedrijfsdatanl/bedrijfsdata-nl-api/collection/rz54v2q/bedrijfsdata-nl-api) |
| [List Companies](actions/list-companies.md) | `GET /companies` | [docs](https://www.postman.com/bedrijfsdatanl/bedrijfsdata-nl-api/request/75odte9/companies) |
| [List Currency Rates](actions/list-currency-rates.md) | `GET /currency` | [docs](https://www.postman.com/bedrijfsdatanl/bedrijfsdata-nl-api/collection/rz54v2q/bedrijfsdata-nl-api) |
| [Lookup BAG Address](actions/lookup-bag-address.md) | `GET /bag` | [docs](https://www.postman.com/bedrijfsdatanl/bedrijfsdata-nl-api/collection/rz54v2q/bedrijfsdata-nl-api) |
| [Lookup City Data](actions/lookup-city-data.md) | `GET /city` | [docs](https://www.postman.com/bedrijfsdatanl/bedrijfsdata-nl-api/collection/rz54v2q/bedrijfsdata-nl-api) |
| [Lookup Company By Domain](actions/lookup-company-by-domain.md) | `GET /rag_domain` | [docs](https://www.postman.com/bedrijfsdatanl/bedrijfsdata-nl-api/collection/rz54v2q/bedrijfsdata-nl-api) |
| [Lookup Company By KVK](actions/lookup-company-by-kvk.md) | `GET /kvk` | [docs](https://www.postman.com/bedrijfsdatanl/bedrijfsdata-nl-api/request/k4v1n7x/kvk) |
| [Lookup DNS Data](actions/lookup-dns-data.md) | `GET /dns` | [docs](https://www.postman.com/bedrijfsdatanl/bedrijfsdata-nl-api/collection/rz54v2q/bedrijfsdata-nl-api) |
| [Lookup LEI](actions/lookup-lei.md) | `GET /lei` | [docs](https://www.postman.com/bedrijfsdatanl/bedrijfsdata-nl-api/collection/rz54v2q/bedrijfsdata-nl-api) |
| [Lookup Page By URL](actions/lookup-page-by-url.md) | `GET /rag_url` | [docs](https://www.postman.com/bedrijfsdatanl/bedrijfsdata-nl-api/collection/rz54v2q/bedrijfsdata-nl-api) |
| [Lookup Postcode](actions/lookup-postcode.md) | `GET /postcode` | [docs](https://www.postman.com/bedrijfsdatanl/bedrijfsdata-nl-api/collection/rz54v2q/bedrijfsdata-nl-api) |
| [Lookup Property Details](actions/lookup-property-details.md) | `GET /property` | [docs](https://www.postman.com/bedrijfsdatanl/bedrijfsdata-nl-api/collection/rz54v2q/bedrijfsdata-nl-api) |
| [Research Company](actions/research-company.md) | `GET /llm` | [docs](https://www.postman.com/bedrijfsdatanl/bedrijfsdata-nl-api/collection/rz54v2q/bedrijfsdata-nl-api) |
| [Search Tenders](actions/search-tenders.md) | `GET /tender` | [docs](https://www.postman.com/bedrijfsdatanl/bedrijfsdata-nl-api/collection/rz54v2q/bedrijfsdata-nl-api) |
| [Search Web Pages](actions/search-web-pages.md) | `GET /rag_search` | [docs](https://www.postman.com/bedrijfsdatanl/bedrijfsdata-nl-api/collection/rz54v2q/bedrijfsdata-nl-api) |
| [Suggest Companies](actions/suggest-companies.md) | `GET /suggest` | [docs](https://www.postman.com/bedrijfsdatanl/bedrijfsdata-nl-api/collection/rz54v2q/bedrijfsdata-nl-api) |
| [Validate BIC](actions/validate-bic.md) | `GET /bic` | [docs](https://www.postman.com/bedrijfsdatanl/bedrijfsdata-nl-api/collection/rz54v2q/bedrijfsdata-nl-api) |
| [Validate Email](actions/validate-email.md) | `GET /email` | [docs](https://www.postman.com/bedrijfsdatanl/bedrijfsdata-nl-api/collection/rz54v2q/bedrijfsdata-nl-api) |
| [Validate IBAN](actions/validate-iban.md) | `GET /iban` | [docs](https://www.postman.com/bedrijfsdatanl/bedrijfsdata-nl-api/collection/rz54v2q/bedrijfsdata-nl-api) |
| [Validate Phone](actions/validate-phone.md) | `GET /phone` | [docs](https://www.postman.com/bedrijfsdatanl/bedrijfsdata-nl-api/collection/rz54v2q/bedrijfsdata-nl-api) |
| [Validate VAT Number](actions/validate-vat-number.md) | `GET /vat` | [docs](https://www.postman.com/bedrijfsdatanl/bedrijfsdata-nl-api/collection/rz54v2q/bedrijfsdata-nl-api) |
| [Validate Website URL](actions/validate-website-url.md) | `GET /url` | [docs](https://www.postman.com/bedrijfsdatanl/bedrijfsdata-nl-api/collection/rz54v2q/bedrijfsdata-nl-api) |
