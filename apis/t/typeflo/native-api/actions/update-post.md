# Update Post with Typeflo

Updates an existing post in Typeflo.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/admin/posts/:id`
- **Base URL:** `https://{subdomain}.typeflo.io/api/headless`
- **Official documentation:** [Update Post](https://typeflo.io/knowledge-base/headless-cms-admin-api-documentation)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The unique ID of the post. |
| `postData.title` | body | `string` | no | The title of the post. |
| `postData.content` | body | `string` | no | The main post content in HTML. |
| `postData.slug` | body | `string` | no | URL-friendly version of the post title. |
| `postData.author` | body | `string` | no | Author ID for the post. |
| `postData.categories[].label` | body | `string` | no | Display label for an assigned category. |
| `postData.categories[].value` | body | `string` | no | Category ID for an assigned category. |
| `postData.tags[].label` | body | `string` | no | Display label for an assigned tag. |
| `postData.tags[].value` | body | `string` | no | Tag ID for an assigned tag. |
| `postData.excerpt` | body | `string` | no | Short summary or introduction for the post. |
| `postData.metatitle` | body | `string` | no | Meta title used in SEO and previews. |
| `postData.metadescription` | body | `string` | no | Meta description used in SEO and previews. |
| `postData.publish_date` | body | `string` | no | Publish date in DD/MM/YYYY format. |
| `postData.toc_status` | body | `boolean` | no | Whether the table of contents is enabled. |
| `postData.is_draft` | body | `boolean` | no | Whether to save the post as a draft. |
| `postData.scheduled` | body | `string` | no | Scheduled publish time in DD/MM/YYYY HH:MM AM/PM format, or null. |
