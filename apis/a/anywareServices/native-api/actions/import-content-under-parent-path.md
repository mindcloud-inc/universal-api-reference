# Import Content Under Parent Path with Anyware Services

Creates a page and imported content under a parent path in Anyware Services.

## Endpoint

- **Method:** `POST`
- **Path:** `/_contentio/import/content/:site/:lang/:path`
- **Base URL:** `https://demo.ametys.org`
- **Official documentation:** [Import Content Under Parent Path](https://docs.ametys.org/fr/plugins/content-io/v1/manuel-utilisateur.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `site` | path | `string` | yes | Target Ametys site name. |
| `lang` | path | `string` | yes | Sitemap language where the page and content will be created. |
| `path` | path | `string` | yes | Optional parent page path documented by Content IO; use this action when importing below a parent page. |
| `content` | body | `file` | yes | XML content file using the Content IO import format. |
