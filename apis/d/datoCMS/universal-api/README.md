# <img src="https://images.mindcloud.co/apps/icons/o0t6ov61lwhl8g3bc5nnle9r1ugz_1771709580523.png" alt="DatoCMS logo" width="28" height="28"> DatoCMS: Universal API

Manage content models, publish assets, localize content, and ship updates.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/datoCMS/latest
- **Category:** Marketing
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
| [List Deploy Events](actions/list-deploy-events.md) | GET |  |

### Field

| Action | Method | Description |
| --- | --- | --- |
| [Create Field](actions/create-field.md) | POST |  |
| [Create Fieldset](actions/create-fieldset.md) | POST |  |
| [Delete Field](actions/delete-field.md) | DELETE |  |
| [Delete Fieldset](actions/delete-fieldset.md) | DELETE |  |
| [Duplicate Field](actions/duplicate-field.md) | POST |  |
| [Get Field](actions/get-field.md) | GET |  |
| [Get Fieldset](actions/get-fieldset.md) | GET |  |
| [List Model Fields](actions/list-model-fields.md) | GET |  |
| [List Model Fieldsets](actions/list-model-fieldsets.md) | GET |  |
| [Update Field](actions/update-field.md) | PUT |  |
| [Update Fieldset](actions/update-fieldset.md) | PUT |  |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Create Upload](actions/create-upload.md) | POST |  |
| [Delete Upload](actions/delete-upload.md) | DELETE |  |
| [Get Upload](actions/get-upload.md) | GET |  |
| [List Referenced Records for Upload](actions/list-referenced-records-for-upload.md) | GET |  |
| [List Uploads](actions/list-uploads.md) | GET |  |
| [Update Upload](actions/update-upload.md) | PUT |  |

### Invitation

| Action | Method | Description |
| --- | --- | --- |
| [List Invitations](actions/list-invitations.md) | GET |  |

### Items

| Action | Method | Description |
| --- | --- | --- |
| [Create Draft Record](actions/create-draft-record.md) | POST |  |
| [Create Scheduled Publication](actions/create-scheduled-publication.md) | POST |  |
| [Create Scheduled Unpublishing](actions/create-scheduled-unpublishing.md) | POST |  |
| [Delete Record](actions/delete-record.md) | DELETE |  |
| [Delete Scheduled Publication](actions/delete-scheduled-publication.md) | DELETE |  |
| [Delete Scheduled Unpublishing](actions/delete-scheduled-unpublishing.md) | DELETE |  |
| [Duplicate Record](actions/duplicate-record.md) | POST |  |
| [Get Record](actions/get-record.md) | GET |  |
| [Get Record Current vs Published State](actions/get-record-current-vs-published-state.md) | GET |  |
| [Get Record Version](actions/get-record-version.md) | GET |  |
| [List Items](actions/list-items.md) | GET |  |
| [List Record Versions](actions/list-record-versions.md) | GET |  |
| [List Referenced Records for Record](actions/list-referenced-records-for-record.md) | GET |  |
| [Publish Record](actions/publish-record.md) | PUT |  |
| [Restore Record Version](actions/restore-record-version.md) | PUT |  |
| [Unpublish Record](actions/unpublish-record.md) | PUT |  |
| [Update Record](actions/update-record.md) | PUT |  |

### Model

| Action | Method | Description |
| --- | --- | --- |
| [Create Model](actions/create-model.md) | POST |  |
| [Delete Model](actions/delete-model.md) | DELETE |  |
| [Duplicate Model](actions/duplicate-model.md) | POST |  |
| [Get Model](actions/get-model.md) | GET |  |
| [List Models](actions/list-models.md) | GET |  |
| [Update Model](actions/update-model.md) | PUT |  |

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [Get Site](actions/get-site.md) | GET |  |
| [List Environments](actions/list-environments.md) | GET |  |
| [List Workflows](actions/list-workflows.md) | GET |  |
| [Update Site Settings](actions/update-site-settings.md) | PUT |  |

### Reports

| Action | Method | Description |
| --- | --- | --- |
| [Get Job Result](actions/get-job-result.md) | GET |  |

### Roles

| Action | Method | Description |
| --- | --- | --- |
| [List Roles](actions/list-roles.md) | GET |  |

### Trigger

| Action | Method | Description |
| --- | --- | --- |
| [List Build Triggers](actions/list-build-triggers.md) | GET |  |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [List Collaborators](actions/list-collaborators.md) | GET |  |

