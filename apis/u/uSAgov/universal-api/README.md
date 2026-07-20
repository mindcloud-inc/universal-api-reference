# <img src="https://images.mindcloud.co/apps/icons/u-sagov_1776453564660.png" alt="USA.gov logo" width="28" height="28"> USA.gov: Universal API

Access USA.gov website traffic downloads and audience analytics

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/uSAgov/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.usa.gov
- **Vendor API docs:** https://www.usa.gov/website-analytics/data/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Download English Site Live Pages](actions/get-usagov-all-pages-people-are-visiting-csv.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uSAgov/latest/actions/get-usagov-all-pages-people-are-visiting-csv?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Website Analytics Report

| Action | Method | Description |
| --- | --- | --- |
| [Download English Site Live Pages](actions/get-usagov-all-pages-people-are-visiting-csv.md) | GET | Downloads live English site pages visited on USA.gov. |
| [Download English Site Device Types](actions/get-usagov-desktop-mobile-tablet-csv.md) | GET | Downloads English site device types from USA.gov. |
| [List English Site Device Models](actions/get-usagov-device-model-json.md) | GET | Retrieves English site device models from USA.gov. |
| [Download Spanish Site Live Pages](actions/get-usagov-es-all-pages-people-are-visiting-csv.md) | GET | Downloads live Spanish site pages visited on USA.gov. |
| [Download Spanish Site Device Types](actions/get-usagov-es-desktop-mobile-tablet-csv.md) | GET | Downloads Spanish site device types from USA.gov. |
| [List Spanish Site Device Models](actions/get-usagov-es-device-model-json.md) | GET | Retrieves Spanish site device models from USA.gov. |
| [List Spanish Site Visitor Languages](actions/get-usagov-es-language-json.md) | GET | Retrieves Spanish site visitor languages from USA.gov. |
| [List Spanish Site Operating Systems](actions/get-usagov-es-operating-systems-json.md) | GET | Retrieves Spanish site operating systems from USA.gov. |
| [List Spanish Site OS and Browser Combinations](actions/get-usagov-es-os-browser-combined-json.md) | GET | Retrieves Spanish site OS and browser combinations from USA.gov. |
| [List Spanish Site Screen Sizes](actions/get-usagov-es-screen-sizes-json.md) | GET | Retrieves Spanish site screen sizes from USA.gov. |
| [Download Spanish Site Top Downloads](actions/get-usagov-es-top-downloads-yesterday-csv.md) | GET | Downloads yesterday's Spanish site top downloads from USA.gov. |
| [List Spanish Site Top Exit Pages](actions/get-usagov-es-top-exit-pages-30-days-json.md) | GET | Retrieves Spanish site top exit pages from USA.gov. |
| [List Spanish Site Top Traffic Sources](actions/get-usagov-es-top-traffic-sources-30-days-json.md) | GET | Retrieves Spanish site top traffic sources from USA.gov. |
| [Get Spanish Site Live Visitors](actions/get-usagov-es-total-people-online-json.md) | GET | Retrieves live Spanish site visitor counts from USA.gov. |
| [List Spanish Site Internet Explorer Versions](actions/get-usagov-es-versions-of-internet-explorer-json.md) | GET | Retrieves Spanish site Internet Explorer versions from USA.gov. |
| [List Spanish Site Windows Versions](actions/get-usagov-es-versions-of-windows-json.md) | GET | Retrieves Spanish site Windows versions from USA.gov. |
| [List Spanish Site Visitors by City](actions/get-usagov-es-visitors-per-city-json.md) | GET | Retrieves Spanish site visitors by city from USA.gov. |
| [List Spanish Site Visitors by Country](actions/get-usagov-es-visitors-per-country-json.md) | GET | Retrieves Spanish site visitors by country from USA.gov. |
| [Get Spanish Site 30-Day Visit Summary](actions/get-usagov-es-visits-over-30-days-json.md) | GET | Retrieves the Spanish site 30-day visit summary from USA.gov. |
| [Download Spanish Site Domain Visits](actions/get-usagov-es-visits-to-all-domains-over-30-days-csv.md) | GET | Downloads 30-day Spanish site domain visits from USA.gov. |
| [List Spanish Site Browsers](actions/get-usagov-es-web-browsers-json.md) | GET | Retrieves Spanish site browsers from USA.gov. |
| [List Spanish Site Windows and Browser Combinations](actions/get-usagov-es-windows-browser-combined-json.md) | GET | Retrieves Spanish site Windows and browser combinations from USA.gov. |
| [List Spanish Site Windows and IE Combinations](actions/get-usagov-es-windows-ie-combined-json.md) | GET | Retrieves Spanish site Windows and IE combinations from USA.gov. |
| [List English Site Visitor Languages](actions/get-usagov-language-json.md) | GET | Retrieves English site visitor languages from USA.gov. |
| [List English Site Operating Systems](actions/get-usagov-operating-systems-json.md) | GET | Retrieves English site operating systems from USA.gov. |
| [List English Site OS and Browser Combinations](actions/get-usagov-os-browser-combined-json.md) | GET | Retrieves English site OS and browser combinations from USA.gov. |
| [List English Site Screen Sizes](actions/get-usagov-screen-sizes-json.md) | GET | Retrieves English site screen sizes from USA.gov. |
| [Download English Site Top Downloads](actions/get-usagov-top-downloads-yesterday-csv.md) | GET | Downloads yesterday's English site top downloads from USA.gov. |
| [List English Site Top Exit Pages](actions/get-usagov-top-exit-pages-30-days-json.md) | GET | Retrieves English site top exit pages from USA.gov. |
| [List English Site Top Traffic Sources](actions/get-usagov-top-traffic-sources-30-days-json.md) | GET | Retrieves English site top traffic sources from USA.gov. |
| [Get English Site Live Visitors](actions/get-usagov-total-people-online-json.md) | GET | Retrieves live English site visitor counts from USA.gov. |
| [List English Site Internet Explorer Versions](actions/get-usagov-versions-of-internet-explorer-json.md) | GET | Retrieves English site Internet Explorer versions from USA.gov. |
| [List English Site Windows Versions](actions/get-usagov-versions-of-windows-json.md) | GET | Retrieves English site Windows versions from USA.gov. |
| [List English Site Visitors by City](actions/get-usagov-visitors-per-city-json.md) | GET | Retrieves English site visitors by city from USA.gov. |
| [List English Site Visitors by Country](actions/get-usagov-visitors-per-country-json.md) | GET | Retrieves English site visitors by country from USA.gov. |
| [Get English Site 30-Day Visit Summary](actions/get-usagov-visits-over-30-days-json.md) | GET | Retrieves the English site 30-day visit summary from USA.gov. |
| [Download English Site Domain Visits](actions/get-usagov-visits-to-all-domains-over-30-days-csv.md) | GET | Downloads 30-day English site domain visits from USA.gov. |
| [List English Site Browsers](actions/get-usagov-web-browsers-json.md) | GET | Retrieves English site browsers from USA.gov. |
| [List English Site Windows and Browser Combinations](actions/get-usagov-windows-browser-combined-json.md) | GET | Retrieves English site Windows and browser combinations from USA.gov. |
| [List English Site Windows and IE Combinations](actions/get-usagov-windows-ie-combined-json.md) | GET | Retrieves English site Windows and IE combinations from USA.gov. |

