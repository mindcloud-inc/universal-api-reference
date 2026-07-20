# DatoCMS: Native API Reference

A consolidated summary of DatoCMS's API configuration and 50 documented operations, with links to official documentation.

- **Official docs:** https://www.datocms.com/docs/content-management-api
- **API base URL:** `https://site-api.datocms.com`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.datocms.com/docs/content-management-api/authentication)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `X-Api-Version` | `3` |

Responses from this API use JSON.

## Pagination

Use `page[limit]` in the query string to set the page size (default 100). Use `page[offset]` in the query string as the record offset; numbering starts at 0.

## Filtering

Send filters in the query string. Supported operators: `between`, `contain`, `eq`, `gt`, `gte`, `lt`, `lte`, `ncontain`, `ne`.

## Sorting

Set the sort field with `order_by` in the query string. Prefix the field name to select its direction. Multiple sort fields can be combined.

## Endpoints (50 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Draft Record](actions/create-draft-record.md) | `POST /items` | [docs](https://www.datocms.com/docs/content-management-api/resources/item/create) |
| [Create Field](actions/create-field.md) | `POST /item-types/:itemTypeId/fields` | [docs](https://www.datocms.com/docs/content-management-api/resources/field/create) |
| [Create Fieldset](actions/create-fieldset.md) | `POST /item-types/:itemTypeId/fieldsets` | [docs](https://www.datocms.com/docs/content-management-api/resources/fieldset/create) |
| [Create Model](actions/create-model.md) | `POST /item-types` | [docs](https://www.datocms.com/docs/content-management-api/resources/item-type/create) |
| [Create Scheduled Publication](actions/create-scheduled-publication.md) | `POST /items/:itemId/scheduled-publication` | [docs](https://www.datocms.com/docs/content-management-api/resources/scheduled-publication/create) |
| [Create Scheduled Unpublishing](actions/create-scheduled-unpublishing.md) | `POST /items/:itemId/scheduled-unpublishing` | [docs](https://www.datocms.com/docs/content-management-api/resources/scheduled-unpublishing/create) |
| [Create Upload](actions/create-upload.md) | `POST /uploads` | [docs](https://www.datocms.com/docs/content-management-api/resources/upload/create) |
| [Delete Field](actions/delete-field.md) | `DELETE /fields/:fieldId` | [docs](https://www.datocms.com/docs/content-management-api/resources/field/destroy) |
| [Delete Fieldset](actions/delete-fieldset.md) | `DELETE /fieldsets/:fieldsetId` | [docs](https://www.datocms.com/docs/content-management-api/resources/fieldset/destroy) |
| [Delete Model](actions/delete-model.md) | `DELETE /item-types/:itemTypeId` | [docs](https://www.datocms.com/docs/content-management-api/resources/item-type/destroy) |
| [Delete Record](actions/delete-record.md) | `DELETE /items/:itemId` | [docs](https://www.datocms.com/docs/content-management-api/resources/item/destroy) |
| [Delete Scheduled Publication](actions/delete-scheduled-publication.md) | `DELETE /items/:itemId/scheduled-publication` | [docs](https://www.datocms.com/docs/content-management-api/resources/scheduled-publication/destroy) |
| [Delete Scheduled Unpublishing](actions/delete-scheduled-unpublishing.md) | `DELETE /items/:itemId/scheduled-unpublishing` | [docs](https://www.datocms.com/docs/content-management-api/resources/scheduled-unpublishing/destroy) |
| [Delete Upload](actions/delete-upload.md) | `DELETE /uploads/:uploadId` | [docs](https://www.datocms.com/docs/content-management-api/resources/upload/destroy) |
| [Duplicate Field](actions/duplicate-field.md) | `POST /fields/:fieldId/duplicate` | [docs](https://www.datocms.com/docs/content-management-api/resources/field/duplicate) |
| [Duplicate Model](actions/duplicate-model.md) | `POST /item-types/:itemTypeId/duplicate` | [docs](https://www.datocms.com/docs/content-management-api/resources/item-type/duplicate) |
| [Duplicate Record](actions/duplicate-record.md) | `POST /items/:itemId/duplicate` | [docs](https://www.datocms.com/docs/content-management-api/resources/item/duplicate) |
| [Get Field](actions/get-field.md) | `GET /fields/:fieldId` | [docs](https://www.datocms.com/docs/content-management-api/resources/field/self) |
| [Get Fieldset](actions/get-fieldset.md) | `GET /fieldsets/:fieldsetId` | [docs](https://www.datocms.com/docs/content-management-api/resources/fieldset/self) |
| [Get Job Result](actions/get-job-result.md) | `GET /job-results/:jobResultId` | [docs](https://www.datocms.com/docs/content-management-api/resources/job-result/self) |
| [Get Model](actions/get-model.md) | `GET /item-types/:itemTypeId` | [docs](https://www.datocms.com/docs/content-management-api/resources/item-type/self) |
| [Get Record](actions/get-record.md) | `GET /items/:itemId` | [docs](https://www.datocms.com/docs/content-management-api/resources/item/self) |
| [Get Record Current vs Published State](actions/get-record-current-vs-published-state.md) | `GET /items/:itemId/current-vs-published-state` | [docs](https://www.datocms.com/docs/content-management-api/resources/item/current_vs_published_state) |
| [Get Record Version](actions/get-record-version.md) | `GET /versions/:versionId` | [docs](https://www.datocms.com/docs/content-management-api/resources/item-version/self) |
| [Get Site](actions/get-site.md) | `GET /site` | [docs](https://www.datocms.com/docs/content-management-api/resources/site/self) |
| [Get Upload](actions/get-upload.md) | `GET /uploads/:uploadId` | [docs](https://www.datocms.com/docs/content-management-api/resources/upload/self) |
| [List Build Triggers](actions/list-build-triggers.md) | `GET /build-triggers` | [docs](https://www.datocms.com/docs/content-management-api/resources/build-trigger/instances) |
| [List Collaborators](actions/list-collaborators.md) | `GET /users` | [docs](https://www.datocms.com/docs/content-management-api/resources/user/instances) |
| [List Deploy Events](actions/list-deploy-events.md) | `GET /build-events` | [docs](https://www.datocms.com/docs/content-management-api/resources/build-event/instances) |
| [List Environments](actions/list-environments.md) | `GET /environments` | [docs](https://www.datocms.com/docs/content-management-api/resources/environment/instances) |
| [List Invitations](actions/list-invitations.md) | `GET /site-invitations` | [docs](https://www.datocms.com/docs/content-management-api/resources/site-invitation/instances) |
| [List Items](actions/list-items.md) | `GET /items` | [docs](https://www.datocms.com/docs/content-management-api/resources/item/instances) |
| [List Model Fields](actions/list-model-fields.md) | `GET /item-types/:model_id_or_api_key/fields` | [docs](https://www.datocms.com/docs/content-management-api/resources/field/instances) |
| [List Model Fieldsets](actions/list-model-fieldsets.md) | `GET /item-types/:model_id_or_api_key/fieldsets` | [docs](https://www.datocms.com/docs/content-management-api/resources/fieldset/instances) |
| [List Models](actions/list-models.md) | `GET /item-types` | [docs](https://www.datocms.com/docs/content-management-api/resources/item-type/instances) |
| [List Record Versions](actions/list-record-versions.md) | `GET /items/:item_id/versions` | [docs](https://www.datocms.com/docs/content-management-api/resources/item-version/instances) |
| [List Referenced Records for Record](actions/list-referenced-records-for-record.md) | `GET /items/:itemId/references` | [docs](https://www.datocms.com/docs/content-management-api/resources/item/references) |
| [List Referenced Records for Upload](actions/list-referenced-records-for-upload.md) | `GET /uploads/:uploadId/references` | [docs](https://www.datocms.com/docs/content-management-api/resources/upload/references) |
| [List Roles](actions/list-roles.md) | `GET /roles` | [docs](https://www.datocms.com/docs/content-management-api/resources/role/instances) |
| [List Uploads](actions/list-uploads.md) | `GET /uploads` | [docs](https://www.datocms.com/docs/content-management-api/resources/upload/instances) |
| [List Workflows](actions/list-workflows.md) | `GET /workflows` | [docs](https://www.datocms.com/docs/content-management-api/resources/workflow/instances) |
| [Publish Record](actions/publish-record.md) | `PUT /items/:itemId/publish` | [docs](https://www.datocms.com/docs/content-management-api/resources/item/publish) |
| [Restore Record Version](actions/restore-record-version.md) | `POST /versions/:versionId/restore` | [docs](https://www.datocms.com/docs/content-management-api/resources/item-version/restore) |
| [Unpublish Record](actions/unpublish-record.md) | `PUT /items/:itemId/unpublish` | [docs](https://www.datocms.com/docs/content-management-api/resources/item/unpublish) |
| [Update Field](actions/update-field.md) | `PUT /fields/:fieldId` | [docs](https://www.datocms.com/docs/content-management-api/resources/field/update) |
| [Update Fieldset](actions/update-fieldset.md) | `PUT /fieldsets/:fieldsetId` | [docs](https://www.datocms.com/docs/content-management-api/resources/fieldset/update) |
| [Update Model](actions/update-model.md) | `PUT /item-types/:itemTypeId` | [docs](https://www.datocms.com/docs/content-management-api/resources/item-type/update) |
| [Update Record](actions/update-record.md) | `PUT /items/:itemId` | [docs](https://www.datocms.com/docs/content-management-api/resources/item/update) |
| [Update Site Settings](actions/update-site-settings.md) | `PUT /site` | [docs](https://www.datocms.com/docs/content-management-api/resources/site/update) |
| [Update Upload](actions/update-upload.md) | `PUT /uploads/:uploadId` | [docs](https://www.datocms.com/docs/content-management-api/resources/upload/update) |
