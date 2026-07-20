# <img src="https://images.mindcloud.co/apps/icons/canva_1773260965573.png" alt="Canva logo" width="28" height="28"> Canva: Universal API

Create, manage, and share Canva designs, folders, and assets

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/canva/latest
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.canva.com
- **Vendor API docs:** https://www.canva.dev/docs/connect/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/canva/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Asset

| Action | Method | Description |
| --- | --- | --- |
| [Get Asset](actions/get-asset.md) | GET | Retrieves details for a Canva asset. |

### Capability

| Action | Method | Description |
| --- | --- | --- |
| [Get User Capabilities](actions/get-user-capabilities.md) | GET | Retrieves the current Canva user's capabilities. |

### Design

| Action | Method | Description |
| --- | --- | --- |
| [Create Design](actions/create-design.md) | POST | Creates a new design in Canva. |
| [Get Design](actions/get-design.md) | GET | Retrieves details for a Canva design. |
| [List Designs](actions/list-designs.md) | GET | Retrieves designs from the current Canva user's projects. |

### Design Export Format

| Action | Method | Description |
| --- | --- | --- |
| [Get Design Export Formats](actions/get-design-export-formats.md) | GET | Retrieves export formats for a Canva design. |

### Design Page

| Action | Method | Description |
| --- | --- | --- |
| [Get Design Pages](actions/get-design-pages.md) | GET | Retrieves pages for a Canva design. |

### Export Job

| Action | Method | Description |
| --- | --- | --- |
| [Create Design Export Job](actions/create-design-export-job.md) | POST | Creates a design export job in Canva. |
| [Get Design Export Job](actions/get-design-export-job.md) | GET | Retrieves a Canva design export job. |

### Folder

| Action | Method | Description |
| --- | --- | --- |
| [Create Folder](actions/create-folder.md) | POST | Creates a new folder in Canva. |
| [Get Folder](actions/get-folder.md) | GET | Retrieves details for a Canva folder. |
| [Update Folder](actions/update-folder.md) | PUT | Updates an existing folder in Canva. |

### Folder Item

| Action | Method | Description |
| --- | --- | --- |
| [List Folder Items](actions/list-folder-items.md) | GET | Retrieves items in a Canva folder. |
| [Move Folder Item](actions/move-folder-item.md) | PUT | Moves an item to another Canva folder. |

### Url Asset Upload Job

| Action | Method | Description |
| --- | --- | --- |
| [Create URL Asset Upload Job](actions/create-url-asset-upload-job.md) | POST | Creates a URL asset upload job in Canva. |
| [Get URL Asset Upload Job](actions/get-url-asset-upload-job.md) | GET | Retrieves a Canva URL asset upload job. |

### Url Import Job

| Action | Method | Description |
| --- | --- | --- |
| [Create URL Import Job](actions/create-url-import-job.md) | POST | Creates a Canva URL import job. |
| [Get URL Import Job](actions/get-url-import-job.md) | GET | Retrieves a Canva URL import job. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves details for the current Canva user. |

### User Profile

| Action | Method | Description |
| --- | --- | --- |
| [Get User Profile](actions/get-user-profile.md) | GET | Retrieves the current Canva user's profile. |

