# USAJOBS Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format USAJOBS expects, and each action page lists the fields available to sort.

## USAJOBS actions that support sorting

- [Search Developer Jobs](actions/search-developer-jobs.md)
- [Search Jobs](actions/search-jobs.md)
- [Search Jobs By Agency](actions/search-jobs-by-agency.md)
- [Search Jobs By Candidate Eligibility](actions/search-jobs-by-candidate-eligibility.md)
- [Search Jobs By Hiring Path](actions/search-jobs-by-hiring-path.md)
- [Search Jobs By Location](actions/search-jobs-by-location.md)
- [Search Jobs By Location Radius](actions/search-jobs-by-location-radius.md)
- [Search Jobs By Occupational Series](actions/search-jobs-by-occupational-series.md)
- [Search Jobs By Pay Grade Range](actions/search-jobs-by-pay-grade-range.md)
- [Search Jobs By Position Title](actions/search-jobs-by-position-title.md)
- [Search Jobs By Salary Range](actions/search-jobs-by-salary-range.md)
- [Search Jobs By Schedule](actions/search-jobs-by-schedule.md)
- [Search Jobs By Security Clearance](actions/search-jobs-by-security-clearance.md)
- [Search Jobs By Travel Requirement](actions/search-jobs-by-travel-requirement.md)
- [Search Jobs By Work Type](actions/search-jobs-by-work-type.md)
- [Search Mission Critical Jobs](actions/search-mission-critical-jobs.md)
- [Search Recently Posted Jobs](actions/search-recently-posted-jobs.md)
- [Search Remote Jobs](actions/search-remote-jobs.md)
