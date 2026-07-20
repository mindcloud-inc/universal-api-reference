# USA.gov: Native API Reference

A consolidated summary of USA.gov's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://www.usa.gov/website-analytics/data/
- **API base URL:** `https://s3-us-gov-west-1.amazonaws.com`

## Authentication

### No Auth

No authentication is required for USA.gov website analytics data downloads.

This API does not require request authentication.

[Official authentication documentation](https://www.usa.gov/website-analytics/data/)

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Download English Site Live Pages](actions/get-usagov-all-pages-people-are-visiting-csv.md) | `GET /cg-446f64bd-3bff-4571-aaf3-22e7fb880b2d/usagov-analytics/en/all-pages-realtime.csv` | [docs](https://www.usa.gov/website-analytics/usagov/data/) |
| [Download English Site Device Types](actions/get-usagov-desktop-mobile-tablet-csv.md) | `GET /cg-446f64bd-3bff-4571-aaf3-22e7fb880b2d/usagov-analytics/en/devices.csv` | [docs](https://www.usa.gov/website-analytics/usagov/data/) |
| [List English Site Device Models](actions/get-usagov-device-model-json.md) | `GET /cg-446f64bd-3bff-4571-aaf3-22e7fb880b2d/usagov-analytics/en/device_model.json` | [docs](https://www.usa.gov/website-analytics/usagov/data/) |
| [Download Spanish Site Live Pages](actions/get-usagov-es-all-pages-people-are-visiting-csv.md) | `GET /cg-446f64bd-3bff-4571-aaf3-22e7fb880b2d/usagov-analytics/es/all-pages-realtime.csv` | [docs](https://www.usa.gov/website-analytics/usagov-en-espanol/data/) |
| [Download Spanish Site Device Types](actions/get-usagov-es-desktop-mobile-tablet-csv.md) | `GET /cg-446f64bd-3bff-4571-aaf3-22e7fb880b2d/usagov-analytics/es/devices.csv` | [docs](https://www.usa.gov/website-analytics/usagov-en-espanol/data/) |
| [List Spanish Site Device Models](actions/get-usagov-es-device-model-json.md) | `GET /cg-446f64bd-3bff-4571-aaf3-22e7fb880b2d/usagov-analytics/es/device_model.json` | [docs](https://www.usa.gov/website-analytics/usagov-en-espanol/data/) |
| [List Spanish Site Visitor Languages](actions/get-usagov-es-language-json.md) | `GET /cg-446f64bd-3bff-4571-aaf3-22e7fb880b2d/usagov-analytics/es/language.json` | [docs](https://www.usa.gov/website-analytics/usagov-en-espanol/data/) |
| [List Spanish Site Operating Systems](actions/get-usagov-es-operating-systems-json.md) | `GET /cg-446f64bd-3bff-4571-aaf3-22e7fb880b2d/usagov-analytics/es/os.json` | [docs](https://www.usa.gov/website-analytics/usagov-en-espanol/data/) |
| [List Spanish Site OS and Browser Combinations](actions/get-usagov-es-os-browser-combined-json.md) | `GET /cg-446f64bd-3bff-4571-aaf3-22e7fb880b2d/usagov-analytics/es/os-browsers.json` | [docs](https://www.usa.gov/website-analytics/usagov-en-espanol/data/) |
| [List Spanish Site Screen Sizes](actions/get-usagov-es-screen-sizes-json.md) | `GET /cg-446f64bd-3bff-4571-aaf3-22e7fb880b2d/usagov-analytics/es/screen-size.json` | [docs](https://www.usa.gov/website-analytics/usagov-en-espanol/data/) |
| [Download Spanish Site Top Downloads](actions/get-usagov-es-top-downloads-yesterday-csv.md) | `GET /cg-446f64bd-3bff-4571-aaf3-22e7fb880b2d/usagov-analytics/es/top-downloads-yesterday.csv` | [docs](https://www.usa.gov/website-analytics/usagov-en-espanol/data/) |
| [List Spanish Site Top Exit Pages](actions/get-usagov-es-top-exit-pages-30-days-json.md) | `GET /cg-446f64bd-3bff-4571-aaf3-22e7fb880b2d/usagov-analytics/es/top-exit-pages-30-days.json` | [docs](https://www.usa.gov/website-analytics/usagov-en-espanol/data/) |
| [List Spanish Site Top Traffic Sources](actions/get-usagov-es-top-traffic-sources-30-days-json.md) | `GET /cg-446f64bd-3bff-4571-aaf3-22e7fb880b2d/usagov-analytics/es/top-traffic-sources-30-days.json` | [docs](https://www.usa.gov/website-analytics/usagov-en-espanol/data/) |
| [Get Spanish Site Live Visitors](actions/get-usagov-es-total-people-online-json.md) | `GET /cg-446f64bd-3bff-4571-aaf3-22e7fb880b2d/usagov-analytics/es/realtime.json` | [docs](https://www.usa.gov/website-analytics/usagov-en-espanol/data/) |
| [List Spanish Site Internet Explorer Versions](actions/get-usagov-es-versions-of-internet-explorer-json.md) | `GET /cg-446f64bd-3bff-4571-aaf3-22e7fb880b2d/usagov-analytics/es/ie.json` | [docs](https://www.usa.gov/website-analytics/usagov-en-espanol/data/) |
| [List Spanish Site Windows Versions](actions/get-usagov-es-versions-of-windows-json.md) | `GET /cg-446f64bd-3bff-4571-aaf3-22e7fb880b2d/usagov-analytics/es/windows.json` | [docs](https://www.usa.gov/website-analytics/usagov-en-espanol/data/) |
| [List Spanish Site Visitors by City](actions/get-usagov-es-visitors-per-city-json.md) | `GET /cg-446f64bd-3bff-4571-aaf3-22e7fb880b2d/usagov-analytics/es/top-cities-90-days.json` | [docs](https://www.usa.gov/website-analytics/usagov-en-espanol/data/) |
| [List Spanish Site Visitors by Country](actions/get-usagov-es-visitors-per-country-json.md) | `GET /cg-446f64bd-3bff-4571-aaf3-22e7fb880b2d/usagov-analytics/es/top-countries-90-days.json` | [docs](https://www.usa.gov/website-analytics/usagov-en-espanol/data/) |
| [Get Spanish Site 30-Day Visit Summary](actions/get-usagov-es-visits-over-30-days-json.md) | `GET /cg-446f64bd-3bff-4571-aaf3-22e7fb880b2d/usagov-analytics/es/traffic-sources-30-days.json` | [docs](https://www.usa.gov/website-analytics/usagov-en-espanol/data/) |
| [Download Spanish Site Domain Visits](actions/get-usagov-es-visits-to-all-domains-over-30-days-csv.md) | `GET /cg-446f64bd-3bff-4571-aaf3-22e7fb880b2d/usagov-analytics/es/all-domains-30-days.csv` | [docs](https://www.usa.gov/website-analytics/usagov-en-espanol/data/) |
| [List Spanish Site Browsers](actions/get-usagov-es-web-browsers-json.md) | `GET /cg-446f64bd-3bff-4571-aaf3-22e7fb880b2d/usagov-analytics/es/browsers.json` | [docs](https://www.usa.gov/website-analytics/usagov-en-espanol/data/) |
| [List Spanish Site Windows and Browser Combinations](actions/get-usagov-es-windows-browser-combined-json.md) | `GET /cg-446f64bd-3bff-4571-aaf3-22e7fb880b2d/usagov-analytics/es/windows-browsers.json` | [docs](https://www.usa.gov/website-analytics/usagov-en-espanol/data/) |
| [List Spanish Site Windows and IE Combinations](actions/get-usagov-es-windows-ie-combined-json.md) | `GET /cg-446f64bd-3bff-4571-aaf3-22e7fb880b2d/usagov-analytics/es/windows-ie.json` | [docs](https://www.usa.gov/website-analytics/usagov-en-espanol/data/) |
| [List English Site Visitor Languages](actions/get-usagov-language-json.md) | `GET /cg-446f64bd-3bff-4571-aaf3-22e7fb880b2d/usagov-analytics/en/language.json` | [docs](https://www.usa.gov/website-analytics/usagov/data/) |
| [List English Site Operating Systems](actions/get-usagov-operating-systems-json.md) | `GET /cg-446f64bd-3bff-4571-aaf3-22e7fb880b2d/usagov-analytics/en/os.json` | [docs](https://www.usa.gov/website-analytics/usagov/data/) |
| [List English Site OS and Browser Combinations](actions/get-usagov-os-browser-combined-json.md) | `GET /cg-446f64bd-3bff-4571-aaf3-22e7fb880b2d/usagov-analytics/en/os-browsers.json` | [docs](https://www.usa.gov/website-analytics/usagov/data/) |
| [List English Site Screen Sizes](actions/get-usagov-screen-sizes-json.md) | `GET /cg-446f64bd-3bff-4571-aaf3-22e7fb880b2d/usagov-analytics/en/screen-size.json` | [docs](https://www.usa.gov/website-analytics/usagov/data/) |
| [Download English Site Top Downloads](actions/get-usagov-top-downloads-yesterday-csv.md) | `GET /cg-446f64bd-3bff-4571-aaf3-22e7fb880b2d/usagov-analytics/en/top-downloads-yesterday.csv` | [docs](https://www.usa.gov/website-analytics/usagov/data/) |
| [List English Site Top Exit Pages](actions/get-usagov-top-exit-pages-30-days-json.md) | `GET /cg-446f64bd-3bff-4571-aaf3-22e7fb880b2d/usagov-analytics/en/top-exit-pages-30-days.json` | [docs](https://www.usa.gov/website-analytics/usagov/data/) |
| [List English Site Top Traffic Sources](actions/get-usagov-top-traffic-sources-30-days-json.md) | `GET /cg-446f64bd-3bff-4571-aaf3-22e7fb880b2d/usagov-analytics/en/top-traffic-sources-30-days.json` | [docs](https://www.usa.gov/website-analytics/usagov/data/) |
| [Get English Site Live Visitors](actions/get-usagov-total-people-online-json.md) | `GET /cg-446f64bd-3bff-4571-aaf3-22e7fb880b2d/usagov-analytics/en/realtime.json` | [docs](https://www.usa.gov/website-analytics/usagov/data/) |
| [List English Site Internet Explorer Versions](actions/get-usagov-versions-of-internet-explorer-json.md) | `GET /cg-446f64bd-3bff-4571-aaf3-22e7fb880b2d/usagov-analytics/en/ie.json` | [docs](https://www.usa.gov/website-analytics/usagov/data/) |
| [List English Site Windows Versions](actions/get-usagov-versions-of-windows-json.md) | `GET /cg-446f64bd-3bff-4571-aaf3-22e7fb880b2d/usagov-analytics/en/windows.json` | [docs](https://www.usa.gov/website-analytics/usagov/data/) |
| [List English Site Visitors by City](actions/get-usagov-visitors-per-city-json.md) | `GET /cg-446f64bd-3bff-4571-aaf3-22e7fb880b2d/usagov-analytics/en/top-cities-90-days.json` | [docs](https://www.usa.gov/website-analytics/usagov/data/) |
| [List English Site Visitors by Country](actions/get-usagov-visitors-per-country-json.md) | `GET /cg-446f64bd-3bff-4571-aaf3-22e7fb880b2d/usagov-analytics/en/top-countries-90-days.json` | [docs](https://www.usa.gov/website-analytics/usagov/data/) |
| [Get English Site 30-Day Visit Summary](actions/get-usagov-visits-over-30-days-json.md) | `GET /cg-446f64bd-3bff-4571-aaf3-22e7fb880b2d/usagov-analytics/en/traffic-sources-30-days.json` | [docs](https://www.usa.gov/website-analytics/usagov/data/) |
| [Download English Site Domain Visits](actions/get-usagov-visits-to-all-domains-over-30-days-csv.md) | `GET /cg-446f64bd-3bff-4571-aaf3-22e7fb880b2d/usagov-analytics/en/all-domains-30-days.csv` | [docs](https://www.usa.gov/website-analytics/usagov/data/) |
| [List English Site Browsers](actions/get-usagov-web-browsers-json.md) | `GET /cg-446f64bd-3bff-4571-aaf3-22e7fb880b2d/usagov-analytics/en/browsers.json` | [docs](https://www.usa.gov/website-analytics/usagov/data/) |
| [List English Site Windows and Browser Combinations](actions/get-usagov-windows-browser-combined-json.md) | `GET /cg-446f64bd-3bff-4571-aaf3-22e7fb880b2d/usagov-analytics/en/windows-browsers.json` | [docs](https://www.usa.gov/website-analytics/usagov/data/) |
| [List English Site Windows and IE Combinations](actions/get-usagov-windows-ie-combined-json.md) | `GET /cg-446f64bd-3bff-4571-aaf3-22e7fb880b2d/usagov-analytics/en/windows-ie.json` | [docs](https://www.usa.gov/website-analytics/usagov/data/) |
