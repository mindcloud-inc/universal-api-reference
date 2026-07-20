# USAJOBS: Native API Reference

A consolidated summary of USAJOBS's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://developer.usajobs.gov/api-reference/
- **API base URL:** `https://data.usajobs.gov`

## Authentication

### API Key

Connect with a USAJOBS API key and the email used for the API request.

### Credentials

- **Authorization Key:** `apiKey` · required
- **User Agent Email:** `userAgentEmail` · required · Email address used when requesting the USAJOBS API key.

Send these headers with each API request:

```http
User-Agent: <userAgentEmail>
Authorization-Key: <apiKey>
```

[Official authentication documentation](https://developer.usajobs.gov/guides/authentication)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `User-Agent` | `{{credentials.userAgentEmail}}` |

The total page count is read from `searchResult.userArea.numberOfPages`.

## Pagination

Use `ResultsPerPage` in the query string to set the page size (default 1; accepted range 1–500). Use `Page` in the query string to choose the page; numbering starts at 1.

## Sorting

Set the sort field with `SortField` in the query string. Set the direction separately with `SortDirection`. Use `Asc` for ascending order and `Desc` for descending order. Only one sort field is accepted.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Historic Announcement Text](actions/get-historic-announcement-text.md) | `GET /api/historicjoa/announcementtext` | [docs](https://developer.usajobs.gov/api-reference/get-api-announcementtext) |
| [List Agencies](actions/list-agencies.md) | `GET /api/codelist/agencysubelements` | [docs](https://developer.usajobs.gov/api-reference/get-codelist-agencysubelements) |
| [List Announcement Closing Types](actions/list-announcement-closing-types.md) | `GET /api/codelist/announcementclosingtypes` | [docs](https://developer.usajobs.gov/api-reference/get-codelist-announcementclosingtype) |
| [List Countries](actions/list-countries.md) | `GET /api/codelist/countries` | [docs](https://developer.usajobs.gov/api-reference/get-codelist-countries) |
| [List Country Subdivisions](actions/list-country-subdivisions.md) | `GET /api/codelist/countrysubdivisions` | [docs](https://developer.usajobs.gov/api-reference/get-codelist-countrysubdivisions) |
| [List Cyber Work Groupings](actions/list-cyber-work-groupings.md) | `GET /api/codelist/cyberworkgroupings` | [docs](https://developer.usajobs.gov/api-reference/get-codelist-cyberworkgroupings) |
| [List Cyber Work Roles](actions/list-cyber-work-roles.md) | `GET /api/codelist/cyberworkroles` | [docs](https://developer.usajobs.gov/api-reference/get-codelist-cyberworkroles) |
| [List Geographic Location Codes](actions/list-geographic-location-codes.md) | `GET /api/codelist/geoloccodes` | [docs](https://developer.usajobs.gov/api-reference/get-codelist-geoloccodes) |
| [List GSA Geo-Loc Codes](actions/list-gsa-geo-loc-codes.md) | `GET /api/codelist/gsageoloccodes` | [docs](https://developer.usajobs.gov/api-reference/get-codelist-gsageoloccodes) |
| [List Hiring Paths](actions/list-hiring-paths.md) | `GET /api/codelist/hiringpaths` | [docs](https://developer.usajobs.gov/api-reference/get-codelist-hiringpaths) |
| [List Historic Job Announcements](actions/list-historic-job-announcements.md) | `GET /api/historicjoa` | [docs](https://developer.usajobs.gov/api-reference/get-api-historicjoa) |
| [List Mission Critical Codes](actions/list-mission-critical-codes.md) | `GET /api/codelist/missioncriticalcodes` | [docs](https://developer.usajobs.gov/api-reference/get-codelist-missioncriticalcodes) |
| [List Occupational Series](actions/list-occupational-series.md) | `GET /api/codelist/occupationalseries` | [docs](https://developer.usajobs.gov/api-reference/get-codelist-occupationalseries) |
| [List Pay Plans](actions/list-pay-plans.md) | `GET /api/codelist/payplans` | [docs](https://developer.usajobs.gov/api-reference/get-codelist-payplans) |
| [List Position Offering Types](actions/list-position-offering-types.md) | `GET /api/codelist/positionofferingtypes` | [docs](https://developer.usajobs.gov/api-reference/get-codelist-positionofferingtypes) |
| [List Position Opening Statuses](actions/list-position-opening-statuses.md) | `GET /api/codelist/positionopeningstatuses` | [docs](https://developer.usajobs.gov/api-reference/get-codelist-positionopeningstatuses) |
| [List Position Schedule Types](actions/list-position-schedule-types.md) | `GET /api/codelist/positionscheduletypes` | [docs](https://developer.usajobs.gov/api-reference/get-codelist-positionscheduletypes) |
| [List Postal Codes](actions/list-postal-codes.md) | `GET /api/codelist/postalcodes` | [docs](https://developer.usajobs.gov/api-reference/get-codelist-postalcodes) |
| [List Security Clearances](actions/list-security-clearances.md) | `GET /api/codelist/securityclearances` | [docs](https://developer.usajobs.gov/api-reference/get-codelist-securityclearances) |
| [List Service Types](actions/list-service-types.md) | `GET /api/codelist/servicetypes` | [docs](https://developer.usajobs.gov/api-reference/get-codelist-servicetypes) |
| [List Travel Percentages](actions/list-travel-percentages.md) | `GET /api/codelist/travelpercentages` | [docs](https://developer.usajobs.gov/api-reference/get-codelist-travelpercentages) |
| [List Who May Apply Codes](actions/list-who-may-apply-codes.md) | `GET /api/codelist/whomayapply` | [docs](https://developer.usajobs.gov/api-reference/get-codelist-whomayapply) |
| [Search Developer Jobs](actions/search-developer-jobs.md) | `GET /api/Search` | [docs](https://developer.usajobs.gov/api-reference/get-api-search) |
| [Search Jobs](actions/search-jobs.md) | `GET /api/Search` | [docs](https://developer.usajobs.gov/api-reference/get-api-search) |
| [Search Jobs By Agency](actions/search-jobs-by-agency.md) | `GET /api/Search` | [docs](https://developer.usajobs.gov/api-reference/get-api-search) |
| [Search Jobs By Candidate Eligibility](actions/search-jobs-by-candidate-eligibility.md) | `GET /api/Search` | [docs](https://developer.usajobs.gov/api-reference/get-api-search) |
| [Search Jobs By Hiring Path](actions/search-jobs-by-hiring-path.md) | `GET /api/Search` | [docs](https://developer.usajobs.gov/api-reference/get-api-search) |
| [Search Jobs By Location](actions/search-jobs-by-location.md) | `GET /api/Search` | [docs](https://developer.usajobs.gov/api-reference/get-api-search) |
| [Search Jobs By Location Radius](actions/search-jobs-by-location-radius.md) | `GET /api/Search` | [docs](https://developer.usajobs.gov/api-reference/get-api-search) |
| [Search Jobs By Occupational Series](actions/search-jobs-by-occupational-series.md) | `GET /api/Search` | [docs](https://developer.usajobs.gov/api-reference/get-api-search) |
| [Search Jobs By Pay Grade Range](actions/search-jobs-by-pay-grade-range.md) | `GET /api/Search` | [docs](https://developer.usajobs.gov/api-reference/get-api-search) |
| [Search Jobs By Position Title](actions/search-jobs-by-position-title.md) | `GET /api/Search` | [docs](https://developer.usajobs.gov/api-reference/get-api-search) |
| [Search Jobs By Salary Range](actions/search-jobs-by-salary-range.md) | `GET /api/Search` | [docs](https://developer.usajobs.gov/api-reference/get-api-search) |
| [Search Jobs By Schedule](actions/search-jobs-by-schedule.md) | `GET /api/Search` | [docs](https://developer.usajobs.gov/api-reference/get-api-search) |
| [Search Jobs By Security Clearance](actions/search-jobs-by-security-clearance.md) | `GET /api/Search` | [docs](https://developer.usajobs.gov/api-reference/get-api-search) |
| [Search Jobs By Travel Requirement](actions/search-jobs-by-travel-requirement.md) | `GET /api/Search` | [docs](https://developer.usajobs.gov/api-reference/get-api-search) |
| [Search Jobs By Work Type](actions/search-jobs-by-work-type.md) | `GET /api/Search` | [docs](https://developer.usajobs.gov/api-reference/get-api-search) |
| [Search Mission Critical Jobs](actions/search-mission-critical-jobs.md) | `GET /api/Search` | [docs](https://developer.usajobs.gov/api-reference/get-api-search) |
| [Search Recently Posted Jobs](actions/search-recently-posted-jobs.md) | `GET /api/Search` | [docs](https://developer.usajobs.gov/api-reference/get-api-search) |
| [Search Remote Jobs](actions/search-remote-jobs.md) | `GET /api/Search` | [docs](https://developer.usajobs.gov/api-reference/get-api-search) |
