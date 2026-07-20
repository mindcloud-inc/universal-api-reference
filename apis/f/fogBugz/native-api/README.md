# FogBugz: Native API Reference

A consolidated summary of FogBugz's API configuration and 12 documented operations, with links to official documentation.

- **Official docs:** https://support.fogbugz.com/en-us/article/55730-fogbugz-api-introduction
- **API base URL:** `{siteUrl}/api`

## Authentication

### API Token

### Credentials

- **API Key:** `apiKey` · required
- **Site URL:** `siteUrl` · required · Your FogBugz site URL, for example https://yourteam.fogbugz.com

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://api.manuscript.com/)

## Endpoints (12 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [List Areas](actions/list-areas.md) | `POST /listAreas` | [docs](https://support.fogbugz.com/en-us/article/55768-fogbugz-xml-api-lists) |
| [List Cases](actions/list-cases.md) | `POST /listCases` | [docs](https://support.fogbugz.com/article/55766-fogbugz-api-listing-searching-and-viewing-cases) |
| [List Categories](actions/list-categories.md) | `POST /listCategories` | [docs](https://support.fogbugz.com/en-us/article/55768-fogbugz-xml-api-lists) |
| [List Filters](actions/list-filters.md) | `POST /listFilters` | [docs](https://support.fogbugz.com/article/55758-fogbugz-xml-api-filters) |
| [List Mailboxes](actions/list-mailboxes.md) | `POST /listMailboxes` | [docs](https://support.fogbugz.com/en-us/article/55768-fogbugz-xml-api-lists) |
| [List Milestones](actions/list-milestones.md) | `POST /listFixFors` | [docs](https://support.fogbugz.com/en-us/article/55768-fogbugz-xml-api-lists) |
| [List People](actions/list-people.md) | `POST /listPeople` | [docs](https://support.fogbugz.com/en-us/article/55768-fogbugz-xml-api-lists) |
| [List Priorities](actions/list-priorities.md) | `POST /listPriorities` | [docs](https://support.fogbugz.com/en-us/article/55768-fogbugz-xml-api-lists) |
| [List Projects](actions/list-projects.md) | `POST /listProjects` | [docs](https://support.fogbugz.com/en-us/article/55768-fogbugz-xml-api-lists) |
| [List Statuses](actions/list-statuses.md) | `POST /listStatuses` | [docs](https://support.fogbugz.com/en-us/article/55768-fogbugz-xml-api-lists) |
| [List Wikis](actions/list-wikis.md) | `POST /listWikis` | [docs](https://support.fogbugz.com/en-us/article/55768-fogbugz-xml-api-lists) |
| [View Case](actions/view-case.md) | `POST /viewCase` | [docs](https://support.fogbugz.com/article/55722-frequently-used-apis) |
