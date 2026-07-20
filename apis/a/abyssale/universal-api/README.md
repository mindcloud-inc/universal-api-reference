# <img src="https://images.mindcloud.co/apps/icons/picto-holder-forest_1774555690509.png" alt="Abyssale logo" width="28" height="28"> Abyssale: Universal API

Create, generate, and manage branded designs and image exports

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/abyssale/latest
- **Actions:** 25
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.abyssale.com
- **Vendor API docs:** https://developers.abyssale.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Fonts](actions/get-fonts.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/abyssale/latest/actions/get-fonts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (25)

### Design

| Action | Method | Description |
| --- | --- | --- |
| [Get Design Details](actions/get-design-details.md) | GET | Retrieves design details from Abyssale. |
| [Get Design Details Advanced](actions/get-design-details-advanced.md) | GET | Retrieves detailed design information from Abyssale. |
| [List Designs](actions/list-designs.md) | GET | Retrieves designs from Abyssale. |
| [List Designs By Category](actions/list-designs-by-category.md) | GET | Retrieves designs from Abyssale by category. |
| [List Designs By Type](actions/list-designs-by-type.md) | GET | Retrieves designs from Abyssale by type. |

### Design Format

| Action | Method | Description |
| --- | --- | --- |
| [Get Design Format Details](actions/get-design-format-details.md) | GET | Retrieves design format details from Abyssale. |

### Duplication Request

| Action | Method | Description |
| --- | --- | --- |
| [Get Duplication Request Status](actions/get-duplication-request-status.md) | GET | Retrieves a template duplication request status from Abyssale. |

### Dynamic Image

| Action | Method | Description |
| --- | --- | --- |
| [Create Dynamic Image URL](actions/create-dynamic-image-url.md) | POST | Creates a dynamic image URL in Abyssale. |

### Export Request

| Action | Method | Description |
| --- | --- | --- |
| [Create Banner Export ZIP](actions/create-banner-export-zip.md) | POST | Exports Abyssale banners as a ZIP archive. |

### File

| Action | Method | Description |
| --- | --- | --- |
| [Get File](actions/get-file.md) | GET | Retrieves a generated file from Abyssale. |

### Font

| Action | Method | Description |
| --- | --- | --- |
| [Get Fonts](actions/get-fonts.md) | GET | Retrieves available fonts from Abyssale. |

### Generated Image

| Action | Method | Description |
| --- | --- | --- |
| [Generate New Visual Version](actions/generate-new-visual-version.md) | POST | Generates a new visual variation in Abyssale. |
| [Generate Single Image](actions/generate-single-image.md) | POST | Generates a single image in Abyssale. |

### Generation Request

| Action | Method | Description |
| --- | --- | --- |
| [Generate All Formats For A Design](actions/generate-all-formats-for-a-design.md) | POST | Generates multi-format assets asynchronously in Abyssale. |
| [Generate Animated GIFs](actions/generate-animated-gifs.md) | POST | Generates animated GIFs asynchronously in Abyssale. |
| [Generate Async Visual Version](actions/generate-async-visual-version.md) | POST | Generates a visual variation asynchronously in Abyssale. |
| [Generate HTML5 Banner Ads](actions/generate-html5-banner-ads.md) | POST | Generates HTML5 banner ads asynchronously in Abyssale. |
| [Generate MP4 Videos](actions/generate-mp4-videos.md) | POST | Generates MP4 videos asynchronously in Abyssale. |
| [Generate Multi-Page Printable PDF](actions/generate-multi-page-printable-pdf.md) | POST | Generates a multi-page printable PDF in Abyssale. |
| [Generate Printable PDF Batch](actions/generate-printable-pdf-batch.md) | POST | Generates printable PDFs asynchronously in Abyssale. |
| [Poll Async Generation Request](actions/poll-async-generation-request.md) | GET | Retrieves an async generation request status from Abyssale. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST | Creates a new project in Abyssale. |
| [List Projects](actions/list-projects.md) | GET | Retrieves projects from Abyssale. |

### Workspace Template

| Action | Method | Description |
| --- | --- | --- |
| [Duplicate Workspace Template](actions/duplicate-workspace-template.md) | POST | Duplicates a workspace template into an Abyssale project. |
| [Duplicate Workspace Template With Custom Name](actions/duplicate-workspace-template-with-custom-name.md) | POST | Duplicates a workspace template into an Abyssale project with a custom name. |

