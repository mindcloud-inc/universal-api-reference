# <img src="https://images.mindcloud.co/apps/icons/cognito-forms_1772651633711.png" alt="Cognito Forms logo" width="28" height="28"> Cognito Forms: Universal API

Build forms, collect data, automate workflows, and generate documents.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/cognitoForms/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.cognitoforms.com
- **Vendor API docs:** https://www.cognitoforms.com/support/475/data-integration/cognito-forms-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Forms](actions/list-forms.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cognitoForms/latest/actions/list-forms?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Document

| Action | Method | Description |
| --- | --- | --- |
| [Get Document](actions/get-document.md) | GET |  |

### Entry

| Action | Method | Description |
| --- | --- | --- |
| [Create Entry](actions/create-entry.md) | POST |  |
| [Create Internal Entry](actions/create-internal-entry.md) | POST |  |
| [Create Public Entry](actions/create-public-entry.md) | POST |  |
| [Create Reviewer Entry](actions/create-reviewer-entry.md) | POST |  |
| [Delete Entry](actions/delete-entry.md) | DELETE |  |
| [Get Entry](actions/get-entry.md) | GET |  |
| [Import Entries Create New](actions/import-entries-create-new.md) | POST |  |
| [Import Entries Sync Entries](actions/import-entries-sync-entries.md) | PUT |  |
| [Import Entries Update Existing](actions/import-entries-update-existing.md) | PUT |  |
| [List View Entries](actions/list-view-entries.md) | GET |  |
| [List View Entries Select Fields](actions/list-view-entries-select-fields.md) | GET |  |
| [List View Entries Select Fields With Count](actions/list-view-entries-select-fields-with-count.md) | GET |  |
| [List View Entries With Count](actions/list-view-entries-with-count.md) | GET |  |
| [Update Entry](actions/update-entry.md) | PUT |  |
| [Update Entry As Internal](actions/update-entry-as-internal.md) | PUT |  |
| [Update Entry As Reviewer](actions/update-entry-as-reviewer.md) | PUT |  |

### File

| Action | Method | Description |
| --- | --- | --- |
| [Get File](actions/get-file.md) | GET |  |
| [Upload File](actions/upload-file.md) | POST |  |

### Form

| Action | Method | Description |
| --- | --- | --- |
| [Get Form Input Schema](actions/get-form-input-schema.md) | GET |  |
| [Get Form Input Schema With Links](actions/get-form-input-schema-with-links.md) | GET |  |
| [Get Form Schema](actions/get-form-schema.md) | GET |  |
| [Get Form Schema With Links](actions/get-form-schema-with-links.md) | GET |  |
| [List Forms](actions/list-forms.md) | GET |  |
| [Set Public Link Availability](actions/set-public-link-availability.md) | PUT |  |
| [Set Public Link Availability Window](actions/set-public-link-availability-window.md) | PUT |  |
| [Set Public Link End Availability](actions/set-public-link-end-availability.md) | PUT |  |
| [Set Public Link Start Availability](actions/set-public-link-start-availability.md) | PUT |  |
| [Set Public Link Unavailable Message](actions/set-public-link-unavailable-message.md) | PUT |  |

### Import Status

| Action | Method | Description |
| --- | --- | --- |
| [Get Import Status](actions/get-import-status.md) | GET |  |

