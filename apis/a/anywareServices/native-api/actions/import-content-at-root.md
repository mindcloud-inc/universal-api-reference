# Import Content At Root with Anyware Services

Creates a page and imported content at the site root in Anyware Services.

## Endpoint

- **Method:** `POST`
- **Path:** `/_contentio/import/content/:site/:lang`
- **Base URL:** `https://demo.ametys.org`
- **Official documentation:** [Import Content At Root](https://docs.ametys.org/fr/plugins/content-io/v1/manuel-utilisateur.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `site` | path | `string` | yes | Target Ametys site name. |
| `lang` | path | `string` | yes | Sitemap language where the page and content will be created. |
| `content` | body | `file` | yes | XML content file using the Content IO import format. |
