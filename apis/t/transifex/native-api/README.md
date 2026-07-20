# Transifex: Native API Reference

A consolidated summary of Transifex's API configuration and 32 documented operations, with links to official documentation.

- **Official docs:** https://developers.transifex.com/
- **API base URL:** `https://rest.api.transifex.com`

## Authentication

### Bearer API Token

Use a Transifex API token generated from User settings > API token. Requests authenticate with Authorization: Bearer <token>.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developers.transifex.com/reference/api-authentication)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/vnd.api+json` |
| `Content-Type` | `application/vnd.api+json` |

Responses from this API use JSON. Response data is read from `data`.

## Endpoints (32 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Project Language](actions/add-project-language.md) | `POST /projects/:project_id/relationships/languages` | [docs](https://developers.transifex.com/reference/post_projects-project-id-relationships-languages.md) |
| [Bulk Update Resource Translations](actions/bulk-update-resource-translations.md) | `PATCH /resource_translations` | [docs](https://developers.transifex.com/reference/patch_resource-translations.md) |
| [Create Project](actions/create-project.md) | `POST /projects` | [docs](https://developers.transifex.com/reference/post_projects.md) |
| [Create Resource](actions/create-resource.md) | `POST /resources` | [docs](https://developers.transifex.com/reference/post_resources.md) |
| [Create Resource String](actions/create-resource-string.md) | `POST /resource_strings` | [docs](https://developers.transifex.com/reference/post_resource-strings.md) |
| [Create Resource String Comment](actions/create-resource-string-comment.md) | `POST /resource_string_comments` | [docs](https://developers.transifex.com/reference/post_resource-string-comments) |
| [Delete Project](actions/delete-project.md) | `DELETE /projects/:project_id` | [docs](https://developers.transifex.com/reference/delete_projects-project-id) |
| [Delete Project Language Relationship](actions/delete-project-language-relationship.md) | `DELETE /projects/:project_id/relationships/languages` | [docs](https://developers.transifex.com/reference/delete_projects-project-id-relationships-languages) |
| [Delete Resource](actions/delete-resource.md) | `DELETE /resources/:resource_id` | [docs](https://developers.transifex.com/reference/delete_resources-resource-id) |
| [Delete Resource String Comment](actions/delete-resource-string-comment.md) | `DELETE /resource_string_comments/:comment_id` | [docs](https://developers.transifex.com/reference/delete_resource-string-comments-comment-id) |
| [Get Language](actions/get-language.md) | `GET /languages/:language_id` | [docs](https://developers.transifex.com/reference/get_languages-language-id.md) |
| [Get Organization](actions/get-organization.md) | `GET /organizations/:organization_id` | [docs](https://developers.transifex.com/reference/get_organizations-organization-id.md) |
| [Get Project](actions/get-project.md) | `GET /projects/:project_id` | [docs](https://developers.transifex.com/reference/get_projects-project-id.md) |
| [Get Resource](actions/get-resource.md) | `GET /resources/:resource_id` | [docs](https://developers.transifex.com/reference/get_resources-resource-id.md) |
| [Get Resource String](actions/get-resource-string.md) | `GET /resource_strings/:resource_string_id` | [docs](https://developers.transifex.com/reference/get_resource-strings-resource-string-id.md) |
| [Get Resource String Comment](actions/get-resource-string-comment.md) | `GET /resource_string_comments/:comment_id` | [docs](https://developers.transifex.com/reference/get_resource-string-comments-comment-id) |
| [Get Resource Translation](actions/get-resource-translation.md) | `GET /resource_translations/:resource_translation_id` | [docs](https://developers.transifex.com/reference/get_resource-translations-resource-translation-id.md) |
| [Get Translation Download](actions/get-translation-download.md) | `GET /resource_translations_async_downloads/:resource_translations_async_download_id` | [docs](https://developers.transifex.com/reference/get_resource-translations-async-downloads-resource-translations-async-download-id.md) |
| [List Languages](actions/list-languages.md) | `GET /languages` | [docs](https://developers.transifex.com/reference/get_languages.md) |
| [List Organizations](actions/list-organizations.md) | `GET /organizations` | [docs](https://developers.transifex.com/reference/get_organizations.md) |
| [List Project Languages](actions/list-project-languages.md) | `GET /projects/:project_id/languages` | [docs](https://developers.transifex.com/reference/get_projects-project-id-languages.md) |
| [List Projects](actions/list-projects.md) | `GET /projects` | [docs](https://developers.transifex.com/reference/get_projects.md) |
| [List Resource String Comments](actions/list-resource-string-comments.md) | `GET /resource_string_comments` | [docs](https://developers.transifex.com/reference/get_resource-string-comments) |
| [List Resource Strings](actions/list-resource-strings.md) | `GET /resource_strings` | [docs](https://developers.transifex.com/reference/get_resource-strings.md) |
| [List Resource Translations](actions/list-resource-translations.md) | `GET /resource_translations` | [docs](https://developers.transifex.com/reference/get_resource-translations.md) |
| [List Resources](actions/list-resources.md) | `GET /resources` | [docs](https://developers.transifex.com/reference/get_resources.md) |
| [Start Translation Download](actions/start-translation-download.md) | `POST /resource_translations_async_downloads` | [docs](https://developers.transifex.com/reference/post_resource-translations-async-downloads.md) |
| [Update Project](actions/update-project.md) | `PATCH /projects/:project_id` | [docs](https://developers.transifex.com/reference/patch_projects-project-id.md) |
| [Update Resource](actions/update-resource.md) | `PATCH /resources/:resource_id` | [docs](https://developers.transifex.com/reference/patch_resources-resource-id.md) |
| [Update Resource String](actions/update-resource-string.md) | `PATCH /resource_strings/:resource_string_id` | [docs](https://developers.transifex.com/reference/patch_resource-strings-resource-string-id.md) |
| [Update Resource String Comment](actions/update-resource-string-comment.md) | `PATCH /resource_string_comments/:comment_id` | [docs](https://developers.transifex.com/reference/patch_resource-string-comments-comment-id) |
| [Update Resource Translation](actions/update-resource-translation.md) | `PATCH /resource_translations/:resource_translation_id` | [docs](https://developers.transifex.com/reference/patch_resource-translations-resource-translation-id.md) |
