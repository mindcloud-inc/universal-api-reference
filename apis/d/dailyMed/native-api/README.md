# DailyMed: Native API Reference

A consolidated summary of DailyMed's API configuration and 12 documented operations, with links to official documentation.

- **Official docs:** https://dailymed.nlm.nih.gov/dailymed/app-support-web-services.cfm
- **API base URL:** `https://dailymed.nlm.nih.gov/dailymed/services/v2`

## Authentication

### No authentication

DailyMed web services are public, read-only GET endpoints and do not require credentials.

This API does not require request authentication.

[Official authentication documentation](https://dailymed.nlm.nih.gov/dailymed/app-support-web-services.cfm)

## API conventions

The total page count is read from `metadata.total_pages`. The current page number is read from `metadata.current_page`.

## Pagination

Use `pagesize` in the query string to set the page size (default 100; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (12 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get SPL XML Document](actions/get-spl-xml-document.md) | `GET /spls/{setid}.xml` | [docs](https://dailymed.nlm.nih.gov/dailymed/webservices-help/v2/spls_setid_api.cfm) |
| [List Application Numbers](actions/list-application-numbers.md) | `GET /applicationnumbers.json` | [docs](https://dailymed.nlm.nih.gov/dailymed/webservices-help/v2/applicationnumbers_api.cfm) |
| [List Drug Classes](actions/list-drug-classes.md) | `GET /drugclasses.json` | [docs](https://dailymed.nlm.nih.gov/dailymed/webservices-help/v2/drugclasses_api.cfm) |
| [List Drug Names](actions/list-drug-names.md) | `GET /drugnames.json` | [docs](https://dailymed.nlm.nih.gov/dailymed/webservices-help/v2/drugnames_api.cfm) |
| [List NDCs](actions/list-ndcs.md) | `GET /ndcs.json` | [docs](https://dailymed.nlm.nih.gov/dailymed/webservices-help/v2/ndcs_api.cfm) |
| [List RxCUIs](actions/list-rxcuis.md) | `GET /rxcuis.json` | [docs](https://dailymed.nlm.nih.gov/dailymed/webservices-help/v2/rxcuis_api.cfm) |
| [List SPL History](actions/list-spl-history.md) | `GET /spls/{setid}/history.json` | [docs](https://dailymed.nlm.nih.gov/dailymed/webservices-help/v2/spls_setid_history_api.cfm) |
| [List SPL Media](actions/list-spl-media.md) | `GET /spls/{setid}/media.json` | [docs](https://dailymed.nlm.nih.gov/dailymed/webservices-help/v2/spls_setid_media_api.cfm) |
| [List SPL NDCs](actions/list-spl-ndcs.md) | `GET /spls/{setid}/ndcs.json` | [docs](https://dailymed.nlm.nih.gov/dailymed/webservices-help/v2/spls_setid_ndcs_api.cfm) |
| [List SPL Packaging](actions/list-spl-packaging.md) | `GET /spls/{setid}/packaging.json` | [docs](https://dailymed.nlm.nih.gov/dailymed/webservices-help/v2/spls_setid_packaging_api.cfm) |
| [List SPLs](actions/list-spls.md) | `GET /spls.json` | [docs](https://dailymed.nlm.nih.gov/dailymed/webservices-help/v2/spls_api.cfm) |
| [List UNIIs](actions/list-uniis.md) | `GET /uniis.json` | [docs](https://dailymed.nlm.nih.gov/dailymed/webservices-help/v2/uniis_api.cfm) |
