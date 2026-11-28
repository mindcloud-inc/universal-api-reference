# <img src="https://images.mindcloud.co/apps/icons/o0t6ov61lwhl8g3bc5nnle9r1ugz_1771709580523.png" alt="DatoCMS logo" width="28" height="28"> DatoCMS: Universal API

Manage content models, publish assets, localize content, and ship updates.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/datoCMS/latest
- **Category:** Website & App Building / CMS
- **Actions:** 50
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.datocms.com/
- **Vendor API docs:** https://www.datocms.com/docs/content-management-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Site](actions/get-site.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/datoCMS/latest/actions/get-site?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (50)

### Events

| Action | Method | Description |
| --- | --- | --- |
| [List Deploy Events](actions/list-deploy-events.md) | GET | Retrieves deploy events from DatoCMS. |

### Field

| Action | Method | Description |
| --- | --- | --- |
| [Create Field](actions/create-field.md) | POST | Creates a new field in DatoCMS. |
| [Create Fieldset](actions/create-fieldset.md) | POST | Creates a new fieldset in DatoCMS. |
| [Delete Field](actions/delete-field.md) | DELETE | Deletes an existing field from DatoCMS. |
| [Delete Fieldset](actions/delete-fieldset.md) | DELETE | Deletes an existing fieldset from DatoCMS. |
| [Duplicate Field](actions/duplicate-field.md) | POST | Creates a duplicate field in DatoCMS. |
| [Get Field](actions/get-field.md) | GET | Retrieves a field from DatoCMS. |
| [Get Fieldset](actions/get-fieldset.md) | GET | Retrieves a fieldset from DatoCMS. |
| [List Model Fields](actions/list-model-fields.md) | GET | Retrieves fields for a model in DatoCMS. |
| [List Model Fieldsets](actions/list-model-fieldsets.md) | GET | Retrieves fieldsets for a model in DatoCMS. |
| [Update Field](actions/update-field.md) | PUT | Updates an existing field in DatoCMS. |
| [Update Fieldset](actions/update-fieldset.md) | PUT | Updates an existing fieldset in DatoCMS. |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Create Upload](actions/create-upload.md) | POST | Creates a new upload in DatoCMS. |
| [Delete Upload](actions/delete-upload.md) | DELETE | Deletes an existing upload from DatoCMS. |
| [Get Upload](actions/get-upload.md) | GET | Retrieves an upload from DatoCMS. |
| [List Referenced Records for Upload](actions/list-referenced-records-for-upload.md) | GET | Retrieves records referencing an upload in DatoCMS. |
| [List Uploads](actions/list-uploads.md) | GET | Retrieves uploads from DatoCMS. |
| [Update Upload](actions/update-upload.md) | PUT | Updates an existing upload in DatoCMS. |

### Invitation

| Action | Method | Description |
| --- | --- | --- |
| [List Invitations](actions/list-invitations.md) | GET | Retrieves invitations from DatoCMS. |

### Items

| Action | Method | Description |
| --- | --- | --- |
| [Create Draft Record](actions/create-draft-record.md) | POST | Creates a new draft record in DatoCMS. |
| [Create Scheduled Publication](actions/create-scheduled-publication.md) | POST | Creates a scheduled publication in DatoCMS. |
| [Create Scheduled Unpublishing](actions/create-scheduled-unpublishing.md) | POST | Creates a scheduled unpublishing in DatoCMS. |
| [Delete Record](actions/delete-record.md) | DELETE | Deletes an existing record from DatoCMS. |
| [Delete Scheduled Publication](actions/delete-scheduled-publication.md) | DELETE | Deletes a scheduled publication from DatoCMS. |
| [Delete Scheduled Unpublishing](actions/delete-scheduled-unpublishing.md) | DELETE | Deletes a scheduled unpublishing from DatoCMS. |
| [Duplicate Record](actions/duplicate-record.md) | POST | Creates a duplicate record in DatoCMS. |
| [Get Record](actions/get-record.md) | GET | Retrieves a record from DatoCMS. |
| [Get Record Current vs Published State](actions/get-record-current-vs-published-state.md) | GET | Retrieves current and published record states from DatoCMS. |
| [Get Record Version](actions/get-record-version.md) | GET | Retrieves a record version from DatoCMS. |
| [List Items](actions/list-items.md) | GET | Retrieves records from DatoCMS. |
| [List Record Versions](actions/list-record-versions.md) | GET | Retrieves record versions from DatoCMS. |
| [List Referenced Records for Record](actions/list-referenced-records-for-record.md) | GET | Retrieves records referenced by a record in DatoCMS. |
| [Publish Record](actions/publish-record.md) | PUT | Publishes a record in DatoCMS. |
| [Restore Record Version](actions/restore-record-version.md) | PUT | Restores a record version in DatoCMS. |
| [Unpublish Record](actions/unpublish-record.md) | PUT | Unpublishes a record in DatoCMS. |
| [Update Record](actions/update-record.md) | PUT | Updates an existing record in DatoCMS. |

### Model

| Action | Method | Description |
| --- | --- | --- |
| [Create Model](actions/create-model.md) | POST | Creates a new model in DatoCMS. |
| [Delete Model](actions/delete-model.md) | DELETE | Deletes an existing model from DatoCMS. |
| [Duplicate Model](actions/duplicate-model.md) | POST | Creates a duplicate model in DatoCMS. |
| [Get Model](actions/get-model.md) | GET | Retrieves a model from DatoCMS. |
| [List Models](actions/list-models.md) | GET | Retrieves models from DatoCMS. |
| [Update Model](actions/update-model.md) | PUT | Updates an existing model in DatoCMS. |

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [Get Site](actions/get-site.md) | GET | Retrieves site settings from DatoCMS. |
| [List Environments](actions/list-environments.md) | GET | Retrieves environments from DatoCMS. |
| [List Workflows](actions/list-workflows.md) | GET | Retrieves workflows from DatoCMS. |
| [Update Site Settings](actions/update-site-settings.md) | PUT | Updates site settings in DatoCMS. |

### Reports

| Action | Method | Description |
| --- | --- | --- |
| [Get Job Result](actions/get-job-result.md) | GET | Retrieves a job result from DatoCMS. |

### Roles

| Action | Method | Description |
| --- | --- | --- |
| [List Roles](actions/list-roles.md) | GET | Retrieves roles from DatoCMS. |

### Trigger

| Action | Method | Description |
| --- | --- | --- |
| [List Build Triggers](actions/list-build-triggers.md) | GET | Retrieves build triggers from DatoCMS. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [List Collaborators](actions/list-collaborators.md) | GET | Retrieves collaborators from DatoCMS. |

