# <img src="https://images.mindcloud.co/apps/icons/jot-url_1775080101986.png" alt="JotUrl logo" width="28" height="28"> JotUrl: Universal API

JotUrl is a link management platform for creating, tracking, and managing branded short URLs, domains, projects, conversion codes, and related analytics through the JotUrl API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/jotUrl/latest
- **Category:** Marketing
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://joturl.com/
- **Vendor API docs:** https://i1.joturl.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Count Domains](actions/count-domains.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jotUrl/latest/actions/count-domains?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [Count Projects](actions/count-projects.md) | GET | Retrieves the number of projects in JotUrl. |
| [Create Project](actions/create-project.md) | POST | Creates a new project in JotUrl. |
| [Delete Project](actions/delete-project.md) | DELETE | Deletes existing projects from JotUrl. |
| [Get Project](actions/get-project.md) | GET | Retrieves a project from JotUrl. |
| [List Projects](actions/list-projects.md) | GET | Retrieves projects from JotUrl. |
| [Update Project](actions/update-project.md) | PUT | Updates an existing project in JotUrl. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Count Conversion Codes](actions/count-conversion-codes.md) | GET | Retrieves the number of conversion codes in JotUrl. |
| [Count Domains](actions/count-domains.md) | GET | Retrieves the number of domains in JotUrl. |
| [Count URLs](actions/count-urls.md) | GET | Retrieves the number of tracking links in JotUrl. |
| [Create Conversion Code](actions/create-conversion-code.md) | POST | Creates a new conversion code in JotUrl. |
| [Create Domain](actions/create-domain.md) | POST | Creates a new domain in JotUrl. |
| [Create Watchdog](actions/create-watchdog.md) | POST | Creates a new watchdog in JotUrl. |
| [Delete Conversion Code](actions/delete-conversion-code.md) | DELETE | Deletes conversion codes from JotUrl. |
| [Delete Domain](actions/delete-domain.md) | DELETE | Deletes an existing domain from JotUrl. |
| [Delete URL](actions/delete-url.md) | DELETE | Deletes tracking links from JotUrl. |
| [Delete Watchdog](actions/delete-watchdog.md) | DELETE | Deletes a watchdog from JotUrl. |
| [Get Conversion Code](actions/get-conversion-code.md) | GET | Retrieves a conversion code from JotUrl. |
| [Get Domain](actions/get-domain.md) | GET | Retrieves a domain from JotUrl. |
| [Get Last URL](actions/get-last-url.md) | GET | Retrieves recent tracking links from JotUrl. |
| [Get URL](actions/get-url.md) | GET | Retrieves a tracking link from JotUrl. |
| [Get Watchdog](actions/get-watchdog.md) | GET | Retrieves a watchdog from JotUrl. |
| [Get Watchdog Stats](actions/get-watchdog-stats.md) | GET | Retrieves watchdog stats from JotUrl. |
| [List Conversion Codes](actions/list-conversion-codes.md) | GET | Retrieves conversion codes from JotUrl. |
| [List Domains](actions/list-domains.md) | GET | Retrieves domains from JotUrl. |
| [List URLs](actions/list-urls.md) | GET | Retrieves tracking links from JotUrl. |
| [Shorten URL](actions/shorten-url.md) | POST | Creates a new tracking link in JotUrl. |
| [Suggest URL Alias](actions/suggest-url-alias.md) | GET | Retrieves suggested URL aliases from JotUrl. |
| [Update Conversion Code](actions/update-conversion-code.md) | PUT | Updates an existing conversion code in JotUrl. |
| [Update Domain](actions/update-domain.md) | PUT | Updates an existing domain in JotUrl. |
| [Update URL](actions/update-url.md) | PUT | Updates an existing tracking link in JotUrl. |

