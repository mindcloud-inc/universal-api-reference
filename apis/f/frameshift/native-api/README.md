# Frameshift: Native API Reference

A consolidated summary of Frameshift's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://mosaic.frameshift.io/api/
- **API base URL:** `https://mosaic.frameshift.io/api`

## Authentication

### API Key

Connect with a Mosaic API bearer token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://mosaic.frameshift.io/api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `data`.

## Pagination

Use `limit` in the query string to set the page size (default 25; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Sorting

Set the sort field with `order_by` in the query string. Set the direction separately with `order_dir`. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Comment](actions/create-comment.md) | `POST /v1/projects/:project_id/conversations/:conversation_id/comments` | [docs](https://mosaic.frameshift.io/api/#api-Collections-PostComment) |
| [Create Conversation](actions/create-conversation.md) | `POST /v1/projects/:project_id/conversations` | [docs](https://mosaic.frameshift.io/api/#api-Collections-CreateConversation) |
| [Create Project](actions/create-project.md) | `POST /v1/projects` | [docs](https://mosaic.frameshift.io/api/#api-Projects-CreateProject) |
| [Create Project File](actions/create-project-file.md) | `POST /v1/projects/:project_id/files` | [docs](https://mosaic.frameshift.io/api/#api-Collections-Create_Project_File) |
| [Create Sample](actions/create-sample.md) | `POST /v1/projects/:project_id/samples` | [docs](https://mosaic.frameshift.io/api/#api-Samples-CreateSample) |
| [Create Sample File](actions/create-sample-file.md) | `POST /v1/projects/:project_id/samples/:sample_id/files` | [docs](https://mosaic.frameshift.io/api/#api-Sample_Files-Create_Sample_File) |
| [Create Task](actions/create-task.md) | `POST /v1/projects/:project_id/tasks` | [docs](https://mosaic.frameshift.io/api/#api-Tasks-CreateTask) |
| [Create Variant Filter](actions/create-variant-filter.md) | `POST /v1/projects/:project_id/variants/filters` | [docs](https://mosaic.frameshift.io/api/#api-Variant_Filters-CreateVariantFilter) |
| [Delete Project](actions/delete-project.md) | `DELETE /v1/projects/:project_id` | [docs](https://mosaic.frameshift.io/api/#api-Collections-DeleteProject) |
| [Delete Sample](actions/delete-sample.md) | `DELETE /v1/projects/:project_id/samples/:sample_id` | [docs](https://mosaic.frameshift.io/api/#api-Samples-DeleteSample) |
| [Delete Variant Filter](actions/delete-variant-filter.md) | `DELETE /v1/projects/:project_id/variants/filters/:variant_filter_id` | [docs](https://mosaic.frameshift.io/api/#api-Variant_Filters-DeleteVariantFilter) |
| [Get Conversation](actions/get-conversation.md) | `GET /v1/projects/:project_id/conversations/:conversation_id` | [docs](https://mosaic.frameshift.io/api/#api-Project_Conversations-GetConversation) |
| [Get Project](actions/get-project.md) | `GET /v1/projects/:project_id` | [docs](https://mosaic.frameshift.io/api/#api-Projects-GetProject) |
| [Get Project File URL](actions/get-project-file-url.md) | `GET /v1/projects/:project_id/files/:file_id/url` | [docs](https://mosaic.frameshift.io/api/#api-Project_Files-GetFile) |
| [Get Sample](actions/get-sample.md) | `GET /v1/projects/:project_id/samples/:sample_id` | [docs](https://mosaic.frameshift.io/api/#api-Samples-GetSample) |
| [Get Sample QC Stats](actions/get-sample-qc-stats.md) | `GET /v1/projects/:project_id/sample-qc-stats` | [docs](https://mosaic.frameshift.io/api/#api-Samples-sampleQcStats) |
| [Get Variant](actions/get-variant.md) | `GET /v1/projects/:project_id/variants/:variant_id` | [docs](https://mosaic.frameshift.io/api/#api-Variants-GetVariant) |
| [Get Variant By Position](actions/get-variant-by-position.md) | `GET /v1/projects/:project_id/variants/position/:chr::start` | [docs](https://mosaic.frameshift.io/api/#api-Variants-GetVariantByPosition) |
| [Get Variant Set](actions/get-variant-set.md) | `GET /v1/projects/:project_id/variants/sets/:variant_set_id` | [docs](https://mosaic.frameshift.io/api/#api-Variants-GetVariantSet) |
| [Get Variant Watchlist](actions/get-variant-watchlist.md) | `GET /v1/projects/:project_id/variants/sets/watchlist` | [docs](https://mosaic.frameshift.io/api/#api-Variants-GetVariantWatchlist) |
| [Import Samples](actions/import-samples.md) | `POST /v1/projects/:project_id/samples/import` | [docs](https://mosaic.frameshift.io/api/#api-Samples-ImportSamples) |
| [List Activity Types](actions/list-activity-types.md) | `GET /v1/activities/types` | [docs](https://mosaic.frameshift.io/api/#api-Activities-GetActivityTypes) |
| [List All Sample Files](actions/list-all-sample-files.md) | `GET /v1/projects/:project_id/samples/files` | [docs](https://mosaic.frameshift.io/api/#api-Sample_Files-Get_All_Sample_Files) |
| [List Conversations](actions/list-conversations.md) | `GET /v1/projects/:project_id/conversations` | [docs](https://mosaic.frameshift.io/api/#api-Project_Conversations-GetConversations) |
| [List Project Activities](actions/list-project-activities.md) | `GET /v1/projects/:project_id/activities` | [docs](https://mosaic.frameshift.io/api/#api-Activities-GetActivities) |
| [List Project Files](actions/list-project-files.md) | `GET /v1/projects/:project_id/files` | [docs](https://mosaic.frameshift.io/api/#api-Project_Files-Get_Project_Files) |
| [List Project Samples](actions/list-project-samples.md) | `GET /v1/projects/:project_id/samples` | [docs](https://mosaic.frameshift.io/api/#api-Samples-GetProjectSamples) |
| [List Project Tasks](actions/list-project-tasks.md) | `GET /v1/projects/:project_id/tasks` | [docs](https://mosaic.frameshift.io/api/#api-Tasks-getProjectTasks) |
| [List Project Variants](actions/list-project-variants.md) | `GET /v1/projects/:project_id/variants/list` | [docs](https://mosaic.frameshift.io/api/#api-Variants-GetProjectVariantsList) |
| [List Projects](actions/list-projects.md) | `GET /v1/projects` | [docs](https://mosaic.frameshift.io/api/#api-Projects-GetProjects) |
| [List Sample Files](actions/list-sample-files.md) | `GET /v1/projects/:project_id/samples/:sample_id/files` | [docs](https://mosaic.frameshift.io/api/#api-Sample_Files-Get_Sample_Files) |
| [List Task Types](actions/list-task-types.md) | `GET /v1/tasks/types` | [docs](https://mosaic.frameshift.io/api/#api-Tasks-getTaskTypes) |
| [List Variant Filters](actions/list-variant-filters.md) | `GET /v1/projects/:project_id/variants/filters` | [docs](https://mosaic.frameshift.io/api/#api-Variant_Filters-GetVariantFilters) |
| [List Variant Sets](actions/list-variant-sets.md) | `GET /v1/projects/:project_id/variants/sets` | [docs](https://mosaic.frameshift.io/api/#api-Variants-GetVariantSets) |
| [Search Variants By Region](actions/search-variants-by-region.md) | `GET /v1/projects/:project_id/variants/by-region` | [docs](https://mosaic.frameshift.io/api/#api-Variants-GetVariantsByRegion) |
| [Update Conversation](actions/update-conversation.md) | `PUT /v1/projects/:project_id/conversations/:conversation_id` | [docs](https://mosaic.frameshift.io/api/#api-Collections-UpdateConversation) |
| [Update Project](actions/update-project.md) | `PUT /v1/projects/:project_id` | [docs](https://mosaic.frameshift.io/api/#api-Collections-UpdateProject) |
| [Update Sample](actions/update-sample.md) | `PUT /v1/projects/:project_id/samples/:sample_id` | [docs](https://mosaic.frameshift.io/api/#api-Samples-PutSample) |
| [Update Task](actions/update-task.md) | `PATCH /v1/projects/:project_id/tasks/:task_id` | [docs](https://mosaic.frameshift.io/api/#api-Tasks-EditTask) |
| [Update Variant Filter](actions/update-variant-filter.md) | `PUT /v1/projects/:project_id/variants/filters/:variant_filter_id` | [docs](https://mosaic.frameshift.io/api/#api-Variant_Filters-UpdateVariantFilter) |
