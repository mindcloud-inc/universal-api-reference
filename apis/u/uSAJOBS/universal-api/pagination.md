# USAJOBS Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model USAJOBS expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uSAJOBS/latest/actions/search-developer-jobs?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## USAJOBS actions that support pagination

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
