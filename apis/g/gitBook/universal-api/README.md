# <img src="https://images.mindcloud.co/apps/icons/git-book_1776794047996.png" alt="GitBook logo" width="28" height="28"> GitBook: Universal API

Manage GitBook spaces, sites, content, and permissions

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/gitBook/latest
- **Category:** Productivity / Knowledge Management
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.gitbook.com
- **Vendor API docs:** https://gitbook.com/docs/developers/gitbook-api/api-reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Authenticated User](actions/get-authenticated-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gitBook/latest/actions/get-authenticated-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Change Request

| Action | Method | Description |
| --- | --- | --- |
| [Create Change Request](actions/create-change-request.md) | POST | Creates a new change request in GitBook. |
| [List Change Requests](actions/list-change-requests.md) | GET | Retrieves change requests from a GitBook space. |

### Collection

| Action | Method | Description |
| --- | --- | --- |
| [Create Collection](actions/create-collection.md) | POST | Creates a new collection in GitBook. |
| [Get Collection](actions/get-collection.md) | GET | Retrieves a collection's details from GitBook. |
| [List Collections](actions/list-collections.md) | GET | Retrieves collections from a GitBook organization. |
| [Update Collection](actions/update-collection.md) | PUT | Updates an existing collection in GitBook. |

### File

| Action | Method | Description |
| --- | --- | --- |
| [List Space Files](actions/list-space-files.md) | GET | Retrieves files from a GitBook space. |

### Member

| Action | Method | Description |
| --- | --- | --- |
| [List Organization Members](actions/list-organization-members.md) | GET | Retrieves members from a GitBook organization. |

### Organization

| Action | Method | Description |
| --- | --- | --- |
| [Get Organization](actions/get-organization.md) | GET | Retrieves organization details from GitBook by ID. |
| [List Organizations](actions/list-organizations.md) | GET | Retrieves organizations available to the GitBook user. |

### Page

| Action | Method | Description |
| --- | --- | --- |
| [Get Space Page](actions/get-space-page.md) | GET | Retrieves a page from a GitBook space. |
| [List Space Pages](actions/list-space-pages.md) | GET | Retrieves pages from a GitBook space. |

### Search Result

| Action | Method | Description |
| --- | --- | --- |
| [Search Site](actions/search-site.md) | GET | Finds content in a GitBook site by query. |

### Site

| Action | Method | Description |
| --- | --- | --- |
| [Create Site](actions/create-site.md) | POST | Creates a new site in GitBook. |
| [Get Site](actions/get-site.md) | GET | Retrieves a site's details from GitBook. |
| [List Sites](actions/list-sites.md) | GET | Retrieves sites from a GitBook organization. |
| [Update Site](actions/update-site.md) | PUT | Updates an existing site in GitBook. |

### Site Space

| Action | Method | Description |
| --- | --- | --- |
| [Add Space To Site](actions/add-space-to-site.md) | POST | Adds an existing space to a GitBook site. |
| [List Site Spaces](actions/list-site-spaces.md) | GET | Retrieves spaces attached to a GitBook site. |

### Space

| Action | Method | Description |
| --- | --- | --- |
| [Create Space](actions/create-space.md) | POST | Creates a new space in GitBook. |
| [Get Space](actions/get-space.md) | GET | Retrieves a space's details from GitBook. |
| [List Spaces](actions/list-spaces.md) | GET | Retrieves spaces from a GitBook organization. |
| [Update Space](actions/update-space.md) | PUT | Updates an existing space in GitBook. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Authenticated User](actions/get-authenticated-user.md) | GET | Retrieves the authenticated user from GitBook. |

