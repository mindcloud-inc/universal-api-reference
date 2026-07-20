# <img src="https://images.mindcloud.co/apps/icons/favicon_1774376427501.png" alt="Templated logo" width="28" height="28"> Templated: Universal API

Generate images, videos, and PDFs from dynamic templates with Templated's API-first editor.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/templated/latest
- **Category:** Marketing
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://templated.io/
- **Vendor API docs:** https://templated.io/docs/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account Information](actions/get-account-information.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/templated/latest/actions/get-account-information?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Folder

| Action | Method | Description |
| --- | --- | --- |
| [Create Folder](actions/create-folder.md) | POST | Creates a new folder in Templated. |
| [Delete Folder](actions/delete-folder.md) | DELETE | Deletes an existing folder from Templated. |
| [List Folders](actions/list-folders.md) | GET | Retrieves all folder records from Templated. |
| [Update Folder](actions/update-folder.md) | PUT | Updates an existing folder in Templated. |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Information](actions/get-account-information.md) | GET | Retrieves detailed account information from Templated. |

### Render

| Action | Method | Description |
| --- | --- | --- |
| [Create Render](actions/create-render.md) | POST | Creates a new render in Templated. |
| [Delete Render](actions/delete-render.md) | DELETE | Deletes an existing render from Templated. |
| [Duplicate Render](actions/duplicate-render.md) | POST | Duplicates an existing render in Templated. |
| [List Renders](actions/list-renders.md) | GET | Retrieves all render records from Templated. |
| [List Template Renders](actions/list-template-renders.md) | GET | Retrieves renders for a template in Templated. |
| [Merge Renders](actions/merge-renders.md) | POST | Merges existing renders together in Templated. |
| [Retrieve Render](actions/retrieve-render.md) | GET | Retrieves detailed render information from Templated. |

### Template

| Action | Method | Description |
| --- | --- | --- |
| [Clone Template](actions/clone-template.md) | POST | Clones an existing template in Templated. |
| [Create Template](actions/create-template.md) | POST | Creates a new template in Templated. |
| [Delete Template](actions/delete-template.md) | DELETE | Deletes an existing template from Templated. |
| [Duplicate Template](actions/duplicate-template.md) | POST | Duplicates an existing template in Templated. |
| [List Folder Templates](actions/list-folder-templates.md) | GET | Retrieves templates in a folder from Templated. |
| [List Template Layers](actions/list-template-layers.md) | GET | Retrieves layers for a template in Templated. |
| [List Template Pages](actions/list-template-pages.md) | GET | Retrieves pages for a template in Templated. |
| [List Templates](actions/list-templates.md) | GET | Retrieves all template records from Templated. |
| [Move Template to Folder](actions/move-template-to-folder.md) | PUT | Moves a template to a folder in Templated. |
| [Update Template](actions/update-template.md) | PUT | Updates an existing template in Templated. |

### Templates

| Action | Method | Description |
| --- | --- | --- |
| [List Gallery Templates](actions/list-gallery-templates.md) | GET | Retrieves gallery template records from Templated. |
| [Retrieve Template](actions/retrieve-template.md) | GET | Retrieves detailed template information from Templated. |

