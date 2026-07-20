# <img src="https://images.mindcloud.co/apps/icons/typeform_1772117881079.png" alt="Typeform logo" width="28" height="28"> Typeform: Universal API

Build forms, collect responses, personalize flows, and analyze results.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/typeform/latest
- **Category:** Productivity / Forms & Surveys
- **Actions:** 48
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.typeform.com
- **Vendor API docs:** https://www.typeform.com/developers/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User Details](actions/get-current-user-details.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/typeform/latest/actions/get-current-user-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (48)

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Download All Files Uploaded by Respondents for a Form](actions/download-all-files-uploaded-by-respondents-for-a-form.md) | GET |  |
| [Get a File from a Response](actions/get-a-file-from-a-response.md) | GET |  |

### Form

| Action | Method | Description |
| --- | --- | --- |
| [Get Form](actions/get-form.md) | GET |  |
| [List Forms](actions/list-forms.md) | GET |  |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Auto-Translate Form](actions/auto-translate-form.md) | POST |  |
| [Create Account Workspace](actions/create-account-workspace.md) | POST |  |
| [Create Form](actions/create-form.md) | POST |  |
| [Create Image](actions/create-image.md) | POST |  |
| [Create or Update Webhook](actions/create-or-update-webhook.md) | PUT |  |
| [Create Theme](actions/create-theme.md) | POST |  |
| [Create Workspace](actions/create-workspace.md) | POST |  |
| [Delete Form](actions/delete-form.md) | DELETE |  |
| [Delete Form Translation](actions/delete-form-translation.md) | DELETE |  |
| [Delete Image](actions/delete-image.md) | DELETE |  |
| [Delete Responses](actions/delete-responses.md) | DELETE |  |
| [Delete Theme](actions/delete-theme.md) | DELETE |  |
| [Delete Webhook](actions/delete-webhook.md) | DELETE |  |
| [Delete Workspace](actions/delete-workspace.md) | DELETE |  |
| [Get Audio Master File (Download)](actions/get-audio-master-file-download.md) | GET |  |
| [Get Video Master File (Download)](actions/get-video-master-file-download.md) | GET |  |
| [List Account Workspaces](actions/list-account-workspaces.md) | GET |  |
| [List Images](actions/list-images.md) | GET |  |
| [List Themes](actions/list-themes.md) | GET |  |
| [List Translation Statuses](actions/list-translation-statuses.md) | GET |  |
| [List Webhooks](actions/list-webhooks.md) | GET |  |
| [Request Audio Master File Generation](actions/request-audio-master-file-generation.md) | POST |  |
| [Request Video Master File Generation](actions/request-video-master-file-generation.md) | POST |  |
| [Retrieve Background by Size](actions/retrieve-background-by-size.md) | GET |  |
| [Retrieve Choice Image by Size](actions/retrieve-choice-image-by-size.md) | GET |  |
| [Retrieve Custom Form Messages](actions/retrieve-custom-form-messages.md) | GET |  |
| [Retrieve Form Translation](actions/retrieve-form-translation.md) | GET |  |
| [Retrieve Image](actions/retrieve-image.md) | GET |  |
| [Retrieve Image by Size](actions/retrieve-image-by-size.md) | GET |  |
| [Retrieve Single Webhook](actions/retrieve-single-webhook.md) | GET |  |
| [Retrieve Theme](actions/retrieve-theme.md) | GET |  |
| [Retrieve Translation Payload](actions/retrieve-translation-payload.md) | GET |  |
| [Retrieve Workspace](actions/retrieve-workspace.md) | GET |  |
| [Update Custom Messages](actions/update-custom-messages.md) | PUT |  |
| [Update Form](actions/update-form.md) | PUT |  |
| [Update Form (Patch)](actions/update-form-patch.md) | PUT |  |
| [Update Form Translation](actions/update-form-translation.md) | PUT |  |
| [Update Theme (Partial Update)](actions/update-theme-partial-update.md) | PUT |  |
| [Update Theme (Whole Definition)](actions/update-theme-whole-definition.md) | PUT |  |
| [Update Workspace](actions/update-workspace.md) | PUT |  |
| [Upload a Video File](actions/upload-a-video-file.md) | POST |  |

### Response

| Action | Method | Description |
| --- | --- | --- |
| [List Responses](actions/list-responses.md) | GET |  |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User Details](actions/get-current-user-details.md) | GET |  |

### Workspace

| Action | Method | Description |
| --- | --- | --- |
| [List Workspaces](actions/list-workspaces.md) | GET |  |

