# <img src="https://images.mindcloud.co/apps/icons/download-4_1774984949248.png" alt="Siteleaf logo" width="28" height="28"> Siteleaf: Universal API

A friendly CMS for static sites with a headless API for content, publishing, and source-file management.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/siteleaf/latest
- **Category:** Website & App Building / CMS
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.siteleaf.com/
- **Vendor API docs:** https://learn.siteleaf.com/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Sites](actions/list-sites.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/siteleaf/latest/actions/list-sites?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Category

| Action | Method | Description |
| --- | --- | --- |
| [List Post Categories](actions/list-post-categories.md) | GET | Retrieves post categories from Siteleaf. |

### Collection

| Action | Method | Description |
| --- | --- | --- |
| [Create Collection](actions/create-collection.md) | POST | Creates a new collection in Siteleaf. |
| [Delete Collection](actions/delete-collection.md) | DELETE | Deletes an existing collection from Siteleaf. |
| [Get Collection](actions/get-collection.md) | GET | Retrieves a collection from Siteleaf. |
| [List Collections](actions/list-collections.md) | GET | Retrieves collections from Siteleaf. |
| [Update Collection](actions/update-collection.md) | PUT | Updates an existing collection in Siteleaf. |

### Collection File

| Action | Method | Description |
| --- | --- | --- |
| [List Collection Files](actions/list-collection-files.md) | GET | Retrieves collection files from Siteleaf. |

### Document

| Action | Method | Description |
| --- | --- | --- |
| [Create Document](actions/create-document.md) | POST | Creates a new document in Siteleaf. |
| [Delete Document](actions/delete-document.md) | DELETE | Deletes an existing document from Siteleaf. |
| [Get Document](actions/get-document.md) | GET | Retrieves a document from Siteleaf. |
| [List Documents](actions/list-documents.md) | GET | Retrieves documents from Siteleaf. |
| [Update Document](actions/update-document.md) | PUT | Updates an existing document in Siteleaf. |

### File

| Action | Method | Description |
| --- | --- | --- |
| [Create or Replace File](actions/create-or-replace-file.md) | PUT | Creates or replaces a file in Siteleaf. |
| [Delete File](actions/delete-file.md) | DELETE | Deletes an existing file from Siteleaf. |
| [Get Files](actions/get-files.md) | GET | Retrieves files or directory contents from Siteleaf. |

### Job

| Action | Method | Description |
| --- | --- | --- |
| [Listen to Job](actions/listen-to-job.md) | GET | Retrieves a job status stream from Siteleaf. |
| [Publish Site](actions/publish-site.md) | POST | Publishes a site in Siteleaf. |

### Page

| Action | Method | Description |
| --- | --- | --- |
| [Create Page](actions/create-page.md) | POST | Creates a new page in Siteleaf. |
| [Delete Page](actions/delete-page.md) | DELETE | Deletes an existing page from Siteleaf. |
| [Get Page](actions/get-page.md) | GET | Retrieves a page from Siteleaf. |
| [List Pages](actions/list-pages.md) | GET | Retrieves pages from Siteleaf. |
| [Update Page](actions/update-page.md) | PUT | Updates an existing page in Siteleaf. |

### Site

| Action | Method | Description |
| --- | --- | --- |
| [Create Site](actions/create-site.md) | POST | Creates a new site in Siteleaf. |
| [Delete Site](actions/delete-site.md) | DELETE | Deletes an existing site from Siteleaf. |
| [Get Site](actions/get-site.md) | GET | Retrieves a site from Siteleaf. |
| [List Sites](actions/list-sites.md) | GET | Retrieves sites from Siteleaf. |
| [Update Site](actions/update-site.md) | PUT | Updates an existing site in Siteleaf. |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [List Post Tags](actions/list-post-tags.md) | GET | Retrieves post tags from Siteleaf. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Authenticated User](actions/get-authenticated-user.md) | GET | Retrieves the authenticated user from Siteleaf. |
| [List Users](actions/list-users.md) | GET | Retrieves users from Siteleaf. |

