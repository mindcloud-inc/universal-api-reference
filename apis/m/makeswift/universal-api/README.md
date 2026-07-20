# <img src="https://images.mindcloud.co/apps/icons/makeswift_1775073820098.png" alt="Makeswift logo" width="28" height="28"> Makeswift: Universal API

Makeswift app for managing sites, pages, locales, and routes through the official Makeswift REST API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/makeswift/latest
- **Category:** Marketing
- **Actions:** 22
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.makeswift.com/
- **Vendor API docs:** https://docs.makeswift.com/developer/reference/api/overview

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Sites](actions/list-sites.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/makeswift/latest/actions/list-sites?connectionId=$CONNECTION_ID&limit=25&offset=0&workspaceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (22)

### Locale

| Action | Method | Description |
| --- | --- | --- |
| [Create Locale](actions/create-locale.md) | POST | Creates a new locale for a site in Makeswift. |
| [Delete Locale](actions/delete-locale.md) | DELETE | Deletes an existing locale from Makeswift. |
| [Get Locale](actions/get-locale.md) | GET | Retrieves a locale from Makeswift. |
| [List Locales](actions/list-locales.md) | GET | Retrieves locales for a site from Makeswift. |
| [Restore Locale](actions/restore-locale.md) | PUT | Restores a deleted locale in Makeswift. |
| [Update Locale](actions/update-locale.md) | PUT | Updates an existing locale in Makeswift. |

### Page

| Action | Method | Description |
| --- | --- | --- |
| [Create Page](actions/create-page.md) | POST | Creates a new page for a site in Makeswift. |
| [Delete Page](actions/delete-page.md) | DELETE | Deletes an existing page from Makeswift. |
| [Get Page](actions/get-page.md) | GET | Retrieves a page from Makeswift. |
| [List Pages](actions/list-pages.md) | GET | Retrieves pages for a site from Makeswift. |
| [Update Page](actions/update-page.md) | PUT | Updates an existing page in Makeswift. |

### Route

| Action | Method | Description |
| --- | --- | --- |
| [Create Route](actions/create-route.md) | POST |  |
| [Delete Route](actions/delete-route.md) | DELETE |  |
| [Get Route](actions/get-route.md) | GET |  |
| [List Routes](actions/list-routes.md) | GET |  |
| [Update Route](actions/update-route.md) | PUT |  |

### Site

| Action | Method | Description |
| --- | --- | --- |
| [Create Site](actions/create-site.md) | POST | Creates a new site in Makeswift. |
| [Delete Site](actions/delete-site.md) | DELETE | Deletes an existing site from Makeswift. |
| [Duplicate Site](actions/duplicate-site.md) | POST | Creates a copy of a site in Makeswift. |
| [Get Site](actions/get-site.md) | GET | Retrieves a site from Makeswift. |
| [List Sites](actions/list-sites.md) | GET | Retrieves sites from Makeswift. |
| [Update Site](actions/update-site.md) | PUT | Updates an existing site in Makeswift. |

