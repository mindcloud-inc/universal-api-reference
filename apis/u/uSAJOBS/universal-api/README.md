# <img src="https://images.mindcloud.co/apps/icons/idu-j9mmj-yb-1777933212174_1777933226472.jpeg" alt="USAJOBS logo" width="28" height="28"> USAJOBS: Universal API

Search and retrieve federal job opportunities

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/uSAJOBS/latest
- **Category:** Human Resources / Recruiting
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.usajobs.gov
- **Vendor API docs:** https://developer.usajobs.gov/api-reference/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Search Developer Jobs](actions/search-developer-jobs.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uSAJOBS/latest/actions/search-developer-jobs?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Announcements

| Action | Method | Description |
| --- | --- | --- |
| [Get Historic Announcement Text](actions/get-historic-announcement-text.md) | GET | Retrieves historic announcement text from USAJOBS. |

### Job Posting

| Action | Method | Description |
| --- | --- | --- |
| [Search Developer Jobs](actions/search-developer-jobs.md) | GET | Finds developer job postings in USAJOBS. |

### Job Postings

| Action | Method | Description |
| --- | --- | --- |
| [List Historic Job Announcements](actions/list-historic-job-announcements.md) | GET | Retrieves historic job announcements from USAJOBS. |
| [List Occupational Series](actions/list-occupational-series.md) | GET | Retrieves occupational series codes from USAJOBS. |
| [Search Jobs](actions/search-jobs.md) | GET | Finds job postings listed in USAJOBS. |
| [Search Jobs By Agency](actions/search-jobs-by-agency.md) | GET | Finds jobs in USAJOBS by agency. |
| [Search Jobs By Candidate Eligibility](actions/search-jobs-by-candidate-eligibility.md) | GET | Finds jobs in USAJOBS by candidate eligibility. |
| [Search Jobs By Hiring Path](actions/search-jobs-by-hiring-path.md) | GET | Finds jobs in USAJOBS by hiring path. |
| [Search Jobs By Location](actions/search-jobs-by-location.md) | GET | Finds jobs in USAJOBS by location. |
| [Search Jobs By Location Radius](actions/search-jobs-by-location-radius.md) | GET | Finds jobs in USAJOBS within a location radius. |
| [Search Jobs By Occupational Series](actions/search-jobs-by-occupational-series.md) | GET | Finds jobs in USAJOBS by occupational series. |
| [Search Jobs By Pay Grade Range](actions/search-jobs-by-pay-grade-range.md) | GET | Finds jobs in USAJOBS by pay grade range. |
| [Search Jobs By Position Title](actions/search-jobs-by-position-title.md) | GET | Finds jobs in USAJOBS by position title. |
| [Search Jobs By Salary Range](actions/search-jobs-by-salary-range.md) | GET | Finds jobs in USAJOBS by salary range. |
| [Search Jobs By Schedule](actions/search-jobs-by-schedule.md) | GET | Finds jobs in USAJOBS by schedule type. |
| [Search Jobs By Security Clearance](actions/search-jobs-by-security-clearance.md) | GET | Finds jobs in USAJOBS by security clearance. |
| [Search Jobs By Travel Requirement](actions/search-jobs-by-travel-requirement.md) | GET | Finds jobs in USAJOBS by travel requirement. |
| [Search Jobs By Work Type](actions/search-jobs-by-work-type.md) | GET | Finds jobs in USAJOBS by work type. |
| [Search Mission Critical Jobs](actions/search-mission-critical-jobs.md) | GET | Finds mission critical jobs in USAJOBS. |
| [Search Recently Posted Jobs](actions/search-recently-posted-jobs.md) | GET | Finds recently posted jobs in USAJOBS. |
| [Search Remote Jobs](actions/search-remote-jobs.md) | GET | Finds remote job postings in USAJOBS. |

### Lists

| Action | Method | Description |
| --- | --- | --- |
| [List Announcement Closing Types](actions/list-announcement-closing-types.md) | GET |  |
| [List Cyber Work Groupings](actions/list-cyber-work-groupings.md) | GET | Retrieves cyber work groupings from USAJOBS. |
| [List Cyber Work Roles](actions/list-cyber-work-roles.md) | GET | Retrieves cyber work roles from USAJOBS. |
| [List Hiring Paths](actions/list-hiring-paths.md) | GET | Retrieves hiring path codes from USAJOBS. |
| [List Mission Critical Codes](actions/list-mission-critical-codes.md) | GET | Retrieves mission critical codes from USAJOBS. |
| [List Pay Plans](actions/list-pay-plans.md) | GET | Retrieves pay plan codes from USAJOBS. |
| [List Position Offering Types](actions/list-position-offering-types.md) | GET | Retrieves position offering types from USAJOBS. |
| [List Security Clearances](actions/list-security-clearances.md) | GET | Retrieves security clearance codes from USAJOBS. |
| [List Service Types](actions/list-service-types.md) | GET | Retrieves service type codes from USAJOBS. |
| [List Travel Percentages](actions/list-travel-percentages.md) | GET | Retrieves travel percentage codes from USAJOBS. |
| [List Who May Apply Codes](actions/list-who-may-apply-codes.md) | GET | Retrieves who may apply codes from USAJOBS. |

### Locations

| Action | Method | Description |
| --- | --- | --- |
| [List Countries](actions/list-countries.md) | GET | Retrieves country code listings from USAJOBS. |
| [List Country Subdivisions](actions/list-country-subdivisions.md) | GET | Retrieves country subdivision codes from USAJOBS. |
| [List Geographic Location Codes](actions/list-geographic-location-codes.md) | GET | Retrieves geographic location codes from USAJOBS. |
| [List GSA Geo-Loc Codes](actions/list-gsa-geo-loc-codes.md) | GET | Retrieves GSA geo-loc codes from USAJOBS. |
| [List Postal Codes](actions/list-postal-codes.md) | GET | Retrieves postal code listings from USAJOBS. |

### Organizations

| Action | Method | Description |
| --- | --- | --- |
| [List Agencies](actions/list-agencies.md) | GET | Retrieves agency subelement codes from USAJOBS. |

### Schedules

| Action | Method | Description |
| --- | --- | --- |
| [List Position Schedule Types](actions/list-position-schedule-types.md) | GET | Retrieves position schedule types from USAJOBS. |

### Statuses

| Action | Method | Description |
| --- | --- | --- |
| [List Position Opening Statuses](actions/list-position-opening-statuses.md) | GET | Retrieves position opening statuses from USAJOBS. |

