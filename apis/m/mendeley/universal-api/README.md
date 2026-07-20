# <img src="https://images.mindcloud.co/apps/icons/id-grk9e-ry-h-1776887248093_1776887265702.png" alt="Mendeley logo" width="28" height="28"> Mendeley: Universal API

Reference manager and academic collaboration platform for managing research libraries, documents, profiles, groups, and annotations through the Mendeley API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/mendeley/latest
- **Category:** Content & Files / Storage
- **Actions:** 28
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.mendeley.com
- **Vendor API docs:** https://dev.mendeley.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get My Profile](actions/get-my-profile.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mendeley/latest/actions/get-my-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (28)

### Annotation

| Action | Method | Description |
| --- | --- | --- |
| [Create Annotation](actions/create-annotation.md) | POST |  |
| [Delete Annotation](actions/delete-annotation.md) | DELETE |  |
| [List Annotations](actions/list-annotations.md) | GET |  |
| [Update Annotation](actions/update-annotation.md) | PUT |  |

### Document

| Action | Method | Description |
| --- | --- | --- |
| [Create Document](actions/create-document.md) | POST |  |
| [Get BibTeX Document](actions/get-bibtex-document.md) | GET |  |
| [Get Document](actions/get-document.md) | GET |  |
| [List BibTeX Documents](actions/list-bibtex-documents.md) | GET |  |
| [List Documents](actions/list-documents-stage3.md) | GET |  |
| [List Folder Documents](actions/list-folder-documents.md) | GET |  |
| [Update Document](actions/update-document.md) | PUT |  |

### Document Lookup

| Action | Method | Description |
| --- | --- | --- |
| [Metadata Lookup](actions/metadata-lookup.md) | GET |  |

### Documents

| Action | Method | Description |
| --- | --- | --- |
| [Delete Trashed Document](actions/delete-trashed-document.md) | DELETE |  |
| [Get Catalog Document](actions/get-catalog-document.md) | GET |  |
| [Get Trashed Document](actions/get-trashed-document.md) | GET |  |
| [List Catalog Documents](actions/list-catalog-documents.md) | GET |  |
| [List Trashed Documents](actions/list-trashed-documents.md) | GET |  |
| [Restore Document](actions/restore-document.md) | PUT |  |
| [Trash Document](actions/trash-document.md) | PUT |  |

### File

| Action | Method | Description |
| --- | --- | --- |
| [List Files](actions/list-files.md) | GET |  |

### Folder

| Action | Method | Description |
| --- | --- | --- |
| [Add Document To Folder](actions/add-document-to-folder.md) | POST |  |
| [Create Folder](actions/create-folder.md) | POST |  |
| [Delete Folder](actions/delete-folder.md) | DELETE |  |
| [List Folders](actions/list-folders.md) | GET |  |
| [Remove Document From Folder](actions/remove-document-from-folder.md) | DELETE |  |
| [Update Folder](actions/update-folder.md) | PUT |  |

### Profile

| Action | Method | Description |
| --- | --- | --- |
| [Get My Profile](actions/get-my-profile.md) | GET |  |

### User Profiles

| Action | Method | Description |
| --- | --- | --- |
| [Update My Profile](actions/update-my-profile.md) | PUT |  |

