# <img src="https://images.mindcloud.co/apps/icons/group_1781722946868.png" alt="Documenterra logo" width="28" height="28"> Documenterra: Universal API

Create corporate knowledge bases, documentation sites, API docs, and technical documentation portals in Documenterra with collaborative editing, publishing, and REST API automation.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/documenterra/latest
- **Category:** Productivity / Knowledge Management
- **Actions:** 19
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://documenterra.ru/
- **Vendor API docs:** https://docs.documenterra.ru/articles/rukovodstvo-polzovatelya-dokumenterry/api-dokumenterry

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Projects](actions/list-projects.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/documenterra/latest/actions/list-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (19)

### Page

| Action | Method | Description |
| --- | --- | --- |
| [Create Page](actions/create-page.md) | POST | Creates a page in Documenterra. |
| [Delete Multiple Pages](actions/delete-multiple-pages.md) | DELETE | Deletes multiple pages from Documenterra. |
| [Delete Page](actions/delete-page.md) | DELETE | Deletes an existing page from Documenterra. |
| [Get Page](actions/get-page.md) | GET | Retrieves a page from Documenterra. |
| [List Pages](actions/list-pages.md) | GET | Retrieves pages from a Documenterra project or publication. |
| [Update Page](actions/update-page.md) | PUT | Updates an existing page in Documenterra. |

### Page View Report

| Action | Method | Description |
| --- | --- | --- |
| [Get Page Views](actions/get-page-views.md) | GET | Retrieves page view reports from Documenterra. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Get Project](actions/get-project.md) | GET | Retrieves a project or publication from Documenterra. |
| [List Projects](actions/list-projects.md) | GET | Retrieves projects and publications from Documenterra. |

### Project User

| Action | Method | Description |
| --- | --- | --- |
| [List Project Access Users](actions/list-project-access-users.md) | GET | Retrieves users with project access from Documenterra. |

### Search Query Report

| Action | Method | Description |
| --- | --- | --- |
| [Get Search Queries](actions/get-search-queries.md) | GET | Retrieves search query reports from Documenterra. |

### Search Result

| Action | Method | Description |
| --- | --- | --- |
| [Search Portal](actions/search-portal.md) | GET | Finds portal content in Documenterra. |

### Tree Element

| Action | Method | Description |
| --- | --- | --- |
| [Delete Tree Element](actions/delete-tree-element.md) | DELETE | Deletes an existing page tree element from Documenterra. |
| [Get Multiple Tree Elements](actions/get-multiple-tree-elements.md) | GET | Retrieves page tree elements from Documenterra. |
| [Get Tree Element](actions/get-tree-element.md) | GET | Retrieves a page tree element from Documenterra. |
| [List Child Tree Elements](actions/list-child-tree-elements.md) | GET | Retrieves child page tree elements from Documenterra. |
| [Update Tree Element](actions/update-tree-element.md) | PUT | Updates an existing page tree element in Documenterra. |

### Tree Folder

| Action | Method | Description |
| --- | --- | --- |
| [Create Tree Folder](actions/create-tree-folder.md) | POST | Creates a page tree folder in Documenterra. |

### User Profile

| Action | Method | Description |
| --- | --- | --- |
| [List User Profiles](actions/list-user-profiles.md) | GET | Retrieves user profiles from Documenterra. |

