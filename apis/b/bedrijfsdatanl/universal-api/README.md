# <img src="https://images.mindcloud.co/apps/icons/bedrijfsdatanl_1774974115483.png" alt="Bedrijfsdata.nl logo" width="28" height="28"> Bedrijfsdata.nl: Universal API

Search, enrich, validate, and retrieve Dutch company and business-related data from Bedrijfsdata.nl.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/bedrijfsdatanl/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 31
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://developers.bedrijfsdata.nl
- **Vendor API docs:** https://www.postman.com/bedrijfsdatanl/bedrijfsdata-nl-api/overview

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Check Password Exposure](actions/check-password-exposure.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bedrijfsdatanl/latest/actions/check-password-exposure?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (31)

### Addresses

| Action | Method | Description |
| --- | --- | --- |
| [Geocode Address](actions/geocode-address.md) | GET |  |
| [Lookup BAG Address](actions/lookup-bag-address.md) | GET |  |
| [Lookup Postcode](actions/lookup-postcode.md) | GET |  |

### Announcements

| Action | Method | Description |
| --- | --- | --- |
| [Find Company News](actions/find-company-news.md) | GET |  |

### Assets

| Action | Method | Description |
| --- | --- | --- |
| [Lookup Property Details](actions/lookup-property-details.md) | GET |  |

### Bank Accounts

| Action | Method | Description |
| --- | --- | --- |
| [Validate BIC](actions/validate-bic.md) | GET |  |
| [Validate IBAN](actions/validate-iban.md) | GET |  |

### Companies

| Action | Method | Description |
| --- | --- | --- |
| [Enrich Company](actions/enrich-company.md) | GET |  |
| [Find Companies At Shared Address](actions/find-companies-at-shared-address.md) | GET |  |
| [Get Corporate Family](actions/get-corporate-family.md) | GET |  |
| [List Companies](actions/list-companies.md) | GET |  |
| [Lookup Company By Domain](actions/lookup-company-by-domain.md) | GET |  |
| [Lookup Company By KVK](actions/lookup-company-by-kvk.md) | GET |  |
| [Research Company](actions/research-company.md) | GET |  |
| [Suggest Companies](actions/suggest-companies.md) | GET |  |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Find Company People](actions/find-company-people.md) | GET |  |

### Custom Objects

| Action | Method | Description |
| --- | --- | --- |
| [Get Site Rank Metrics](actions/get-site-rank-metrics.md) | GET |  |
| [Get Web Rank Summary](actions/get-web-rank-summary.md) | GET |  |
| [Lookup DNS Data](actions/lookup-dns-data.md) | GET |  |

### Emails

| Action | Method | Description |
| --- | --- | --- |
| [Validate Email](actions/validate-email.md) | GET |  |

### Exchange Rates

| Action | Method | Description |
| --- | --- | --- |
| [List Currency Rates](actions/list-currency-rates.md) | GET |  |

### Job Postings

| Action | Method | Description |
| --- | --- | --- |
| [Find Company Vacancies](actions/find-company-vacancies.md) | GET |  |

### Locations

| Action | Method | Description |
| --- | --- | --- |
| [Lookup City Data](actions/lookup-city-data.md) | GET |  |

### Organizations

| Action | Method | Description |
| --- | --- | --- |
| [Lookup LEI](actions/lookup-lei.md) | GET |  |
| [Validate VAT Number](actions/validate-vat-number.md) | GET |  |

### Pages

| Action | Method | Description |
| --- | --- | --- |
| [Lookup Page By URL](actions/lookup-page-by-url.md) | GET |  |
| [Search Web Pages](actions/search-web-pages.md) | GET |  |
| [Validate Website URL](actions/validate-website-url.md) | GET |  |

### Phone Numbers

| Action | Method | Description |
| --- | --- | --- |
| [Validate Phone](actions/validate-phone.md) | GET |  |

### Request For Quotes

| Action | Method | Description |
| --- | --- | --- |
| [Search Tenders](actions/search-tenders.md) | GET |  |

### Secrets

| Action | Method | Description |
| --- | --- | --- |
| [Check Password Exposure](actions/check-password-exposure.md) | GET |  |

